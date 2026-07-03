# Zelfregulatie

Dit is een NOLAI co-creatie project. Voor meer details over het co-creatie project, zie hier: https://www.ru.nl/onderzoek/onderzoeksprojecten/zelfregulatie-tijdens-het-schrijven

Deze repository is een bundeling van de onderliggende software. Deels is deze buiten het co-creatie project ontwikkeld en deels speciaal voor dit co-creatie project.

[De Flora backend](FLoRA_backend/) en het [Flora dashboard](flora-admin2/) bestonden al voor het co-creatie project en zijn veel breder inzetbaar. De [srl (self regulated learning) API](srl-api/) en het [srl Dashboard](srl-dashboard/) zijn voor dit project ontwikkeld.

## Benodigheden om zelf het project te reproduceren

Om het gehele project na te maken en de software te hergebruiken vraagt enige extra draaiende software:

- Een moodle omgeving, de plek waar leerlingen een schrijopdracht maken.
- Een (mysql) database, gebruikt door Moodle, de Flora backend en de srl API.
- Een redis instantie voor de Flora backend.
- Een elastic search instantie voor de Flora backend.
- Een kafka instantie voor de Flora backend.
- Een zookeeper instantie voor kafka.
- Een [T-Scan](https://github.com/CentreForDigitalHumanities/tscan) instantie voor de srl API.

Daarnaast is voor de srl API toegang nodig to [LIWC](https://www.liwc.app/), dit vereist een abbonement.

## Configuratie

De meeste configuratie instructies staan in de sub-projecten zelf. Maar er zijn een aantal dingen die misschien niet meteen duidelijk zijn.

### Moodle configuratie

Voor de moodle configuratie is een de [Generico filter plugin](https://moodle.org/plugins/filter_generico) nodig. Deze wordt gebruikt om de [Flora javascript templates](FLoRA_backend/src/main/resources/templates/generico_and_additional_config) op de opdracht pagina's in te laden zodat deze script het schrijfproces kunnen tracken.

### Flora backend configuratie

De configuratie van de Flora backend zit deels in de java code dit zit in [MyConstant.java](FLoRA_backend/src/main/java/com/monash/flora_backend/constant/MyConstant.java) en [FLoRABackendApplication.java](FLoRA_backend/src/main/java/com/monash/flora_backend/FLoRABackendApplication.java).

Voor het aanpassen van script functionaliteit kan ook [general_config_all_course.html](FLoRA_backend/src/main/resources/templates/generico_and_additional_config/general_config_all_course.html) aangepast worden.

## Vragen

Voor vragen over de technische aspecten van het project neem vooral contact op met het NOLAI tech team: nolai@science.ru.nl

## Funding

Dit project is mede gefinancierd door het [Nationaal Onderwijslab AI](https://nolai.nl)

![NOLAI logo](Logo_NOLAI_NL.jpg "NOLAI logo")
