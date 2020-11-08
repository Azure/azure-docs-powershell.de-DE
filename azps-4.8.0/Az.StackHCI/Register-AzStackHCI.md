---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: c09c4b4c8d71d90bbbac0771c75ea3ea51ee05dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173397"
---
# Register-AzStackHCI

## Synopsis
Register-AzStackHCI erstellt eine Microsoft. AzureStackHCI-Cloud-Ressource, die den lokalen Cluster darstellt, und registriert den lokalen Cluster mit Azure.

## Syntax

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## Beschreibung
Register-AzStackHCI erstellt eine Microsoft. AzureStackHCI-Cloud-Ressource, die den lokalen Cluster darstellt, und registriert den lokalen Cluster mit Azure.

## Beispiele

### Beispiel 1
```
Invoking on one of the cluster node.
```

C:\PS \> Register-AzStackHCI-Subscription-"12a0f531-56CB-4340-9501-257726d741fd" Ergebnis: Success Resourcen:/Subscriptions/12a0f531-56CB-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/

### Beispiel 2
```
Invoking from the management node
```

C:\PS \> Register-AzStackHCI-Subscription-"12a0f531-56CB-4340-9501-257726d741fd"-Computername ClusterNode1 Ergebnis: Success Resourcen:/Subscriptions/12a0f531-56CB-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/

### Beispiel 3
```
Invoking from WAC
```

C:\PS \> Register-AzStackHCI-Subscription-"12a0f531-56CB-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-Accounting user1@corp1.com -Region westus-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG Ergebnis: PendingForAdminConsent/Subscriptions/12a0f531-56CB-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster3 https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview : PortalResourceURL https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/

### Beispiel 4
```
Invoking with all the parameters
```

C:\PS \> Register-AzStackHCI-Abonnement-"12a0f531-56CB-4340-9501-257726d741fd"-Region westus-resourceName HciCluster1-tenantal "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken ACee.. rerrer-Accounting user1@corp1.com -environmentname AzureCloud-Computername node1hci-Get-Credential Ergebnis: Success Resourcen:/Subscriptions/12a0f531-56CB-4340-9501-257726d741fd/resourceGroups/HciClusterRG/Providers/Microsoft.AzureStackHCI/Clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/

## Parameter

### -Abonnement-Nr
Gibt das Azure-Abonnement zum Erstellen der Ressource an.
Dies ist der einzige obligatorische Parameter.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region
Gibt den Bereich zum Erstellen der Ressource an.
Standard ist eastus.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Gibt den Ressourcennamen der in Azure erstellten Ressource an.
Wenn nicht angegeben, wird der lokale Clustername verwendet.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mandanten-Nr
Gibt die Azure-Mandanten-Nr an.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Azure-Ressourcengruppe an.
Wenn nicht angegeben, \<LocalClusterName\> wird RG als Ressourcengruppenname verwendet.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArmAccessToken
Gibt das Zugriffstoken für den Arm an.
Wenn Sie dies zusammen mit GraphAccessToken und der Konto-Nr angeben, wird eine Azure Interactive-Anmeldung vermieden.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
Gibt das Diagramm Zugriffstoken an.
Wenn Sie dies zusammen mit ArmAccessToken und der Konto-Nr angeben, wird eine Azure Interactive-Anmeldung vermieden.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Konto-Nr
Gibt das Zugriffstoken für den Arm an.
Wenn Sie dies zusammen mit ArmAccessToken und GraphAccessToken angeben, wird eine Azure Interactive-Anmeldung vermieden.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Umgebungsname
Gibt die Azure-Umgebung an.
Der Standardwert ist AzureCloud.
Gültige Werte sind AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -Computername
Gibt den Clusternamen oder einen Clusterknoten in einem lokalen Cluster an, der für Azure registriert wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### – Anmeldeinformationen
Gibt die Anmeldeinformationen für den Computername an.
Standard ist der aktuelle Benutzer, der das Cmdlet ausführt.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

## Ausgaben

### PSCustomObject. Gibt die folgenden Eigenschaften in PSCustomObject zurück.
### Ergebnis: Erfolg oder Fehler oder PendingForAdminConsent oder storniert.
### Resourcen-ID: Ressourcen-ID der in Azure erstellten Ressource.
### PortalResourceURL: Azure-Portal-Ressourcen-URL.
### PortalAADAppPermissionsURL: Azure Portal URL für die Aad-App-Berechtigungsseite.
## Notizen

## Verwandte Links
