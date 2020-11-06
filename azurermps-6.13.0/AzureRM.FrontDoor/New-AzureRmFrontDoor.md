---
externe Hilfedatei: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml Modul Name: AzureRM. Haustür Online-Version: die entsprechende URL sollte wie folgt lauten: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor Schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md
---

# <a name="new-azurermfrontdoor"></a>New-AzureRmFrontDoor

## <a name="synopsis"></a>Synopsis
Erstellen eines neuen Azure Front Door Load Balancer

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <a name="syntax"></a>Syntax

```
New-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <a name="description"></a>Beschreibung
Das Cmdlet **New-AzureRmFrontDoor** erstellt ein neues Azure Front Door Load Balancer in der angegebenen Ressourcengruppe unter Aktuelles Abonnement.

## <a name="examples"></a>Beispiele

### <a name="example-1-create-a-front-door-based-on-given-parameters"></a>Beispiel 1: Erstellen einer Haustür basierend auf bestimmten Parametern
```powershell
PS C:\> New-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

Erstellen einer Haustür basierend auf bestimmten Parametern

## <a name="parameters"></a>Parameter

### <a name="-backendpool"></a>-BackendPool
Backendpools ist für Routingregel verfügbar.

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-defaultprofile"></a>-DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-enabledstate"></a>-EnabledState
EnabledState des Front Door Load Balancer.
Standardwert ist aktiviert

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-frontendendpoint"></a>-FrontendEndpoint
Für Routingregel verfügbare Frontend-Endpunkte.

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-healthprobesetting"></a>-HealthProbeSetting
Einstellungen für Integritäts Prüfspitzen, die dieser Haustür Instanz zugeordnet sind.

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-loadbalancingsetting"></a>-LoadBalancingSetting
Lastenausgleichseinstellungen, die dieser Haustür Instanz zugeordnet sind.

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-name"></a>-Name
Name der Haustüre

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-resourcegroupname"></a>-ResourceGroupName
Der Ressourcengruppenname, in dem die Haustür erstellt wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-routingrule"></a>-RoutingRule
Diesem Haustür zugeordnete Routing Regeln

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-tag"></a>-Tag
Die Tags werden dem Haustür zugeordnet.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-confirm"></a>-Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="-whatif"></a>-WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <a name="commonparameters"></a>CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## <a name="inputs"></a>Eingaben

### <a name="systemstring"></a>System. String

## <a name="outputs"></a>Ausgaben

### <a name="microsoftazurecommandsfrontdoormodelspsfrontdoor"></a>Microsoft. Azure. Commands. Haustür. Models. PSFrontDoor

## <a name="notes"></a>Notizen

## <a name="related-links"></a>Verwandte Links

[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Satz-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [Neu – AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [Neu – AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [Neu – AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [Neu – AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [Neu – AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)
