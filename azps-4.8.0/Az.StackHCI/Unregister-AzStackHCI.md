---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173396"
---
# Unregister-AzStackHCI

## Synopsis
Unregister-AzStackHCI löscht die Microsoft. AzureStackHCI-Cloud-Ressource, die den lokalen Cluster darstellt, und hebt die Registrierung des lokalen Clusters mit Azure auf.
Die im Cluster verfügbaren registrierten Informationen werden verwendet, um die Registrierung des Clusters aufzuheben, wenn keine Parameter übergeben werden.

## Syntax

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Unregister-AzStackHCI löscht die Microsoft. AzureStackHCI-Cloud-Ressource, die den lokalen Cluster darstellt, und hebt die Registrierung des lokalen Clusters mit Azure auf.
Die im Cluster verfügbaren registrierten Informationen werden verwendet, um die Registrierung des Clusters aufzuheben, wenn keine Parameter übergeben werden.

## Beispiele

### Beispiel 1
```
Invoking on one of the cluster node
```

C:\PS \> Unregister-AzStackHCI-Ergebnis: Erfolg

### Beispiel 2
```
Invoking from the management node
```

C:\PS \> Unregister-AzStackHCI-Computername ClusterNode1 Ergebnis: Erfolg

### Beispiel 3
```
Invoking from WAC
```

C:\PS \> Unregister-AzStackHCI-Abonnement-"12a0f531-56CB-4340-9501-257726d741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken acyee.. rerrer-Accounting user1@corp1.com -resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG-bestätigen: $false Ergebnis: Erfolg

### Beispiel 4
```
Invoking with all the parameters
```

C:\PS \> Unregister-AzStackHCI-Abonnement-"12a0f531-56CB-4340-9501-257726d741fd"-resourceName HciCluster1-tenantal "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ere =-GraphAccessToken ACee.. rerrer-Account-Nr user1@corp1.com -environmentname AzureCloud-Computername node1hci-Get-Credential Ergebnis für Anmeldeinformationen: Erfolg

## Parameter

### -Abonnement-Nr
Gibt das Azure-Abonnement zum Erstellen der Ressource an.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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
Position: 2
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
Position: 3
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
Position: 4
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
Position: 5
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
Position: 6
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
Position: 7
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
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -Computername
Gibt einen der Clusterknoten in einem lokalen Cluster an, der für Azure registriert wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
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
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

## Ausgaben

### PSCustomObject. Gibt die folgenden Eigenschaften in PSCustomObject zurück.
### Ergebnis: Erfolg oder Fehler oder storniert.
## Notizen

## Verwandte Links
