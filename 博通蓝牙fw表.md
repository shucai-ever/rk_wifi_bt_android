```
#define FW_TABLE_VERSION "v1.1 20161117"
static const fw_auto_detection_entry_t fw_auto_detection_table[] = {
    {"4343A0","BCM43438A0"},    //AP6212
    {"BCM43430A1","BCM43438A1"}, //AP6212A
    {"BCM20702A","BCM20710A1"}, //AP6210B
    {"BCM4335C0","BCM4339A0"}, //AP6335
    {"BCM4330B1","BCM40183B2"}, //AP6330
    {"BCM4324B3","BCM43241B4"}, //AP62X2
    {"BCM4350C0","BCM4354A1"}, //AP6354
    {"BCM4354A2","BCM4356A2"}, //AP6356
    {"BCM4345C0","BCM4345C0"}, //AP6255
//    {"BCM43341B0","BCM43341B0"}, //AP6234
//    {"BCM2076B1","BCM2076B1"}, //AP6476
	{"BCM43430B0","BCM4343B0"}, //AP6236
	{"BCM4359C0","BCM4359C0"},	//AP6359
	{"BCM4349B1","BCM4359B1"},	//AP6359
    {(const char *) NULL, NULL}
};
```

```
    p_entry = (fw_auto_detection_entry_t *)fw_auto_detection_table;
    while (p_entry->chip_id != NULL)
    {
        if (strstr(p_chip_id_str, p_entry->chip_id)!=NULL)
        {
            strcpy(p_chip_id_str,p_entry->updated_chip_id);
            break;
        }
        p_entry++;
    }
```

