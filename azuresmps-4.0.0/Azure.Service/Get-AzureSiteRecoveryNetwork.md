---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a5701fc6308f1884bbf0237887a223a62a58669
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411584"
---
# Get-AzureSiteRecoveryNetwork

## SYNOPSIS
Ruft Informationen zu den Netzwerken ab, die von der Websitewiederherstellung für den aktuellen Tresor verwaltet werden.

## SYNTAX

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzureSiteRecoveryNetwork"** ruft Informationen zu Azure Site Recovery Networks für den aktuellen Websitewiederherstellungstresor ab.

## BEISPIELE

### Beispiel 1: Websitewiederherstellungsnetzwerke erhalten
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetwork -Server $Servers[0]
Name                : phase2RecoveryVMNetwork
ID                  : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
FabricObjectID      : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}

Name                : phase2PrimaryVMNetwork
ID                  : d903e2c6-3141-4cef-bfe1-04616cd43cbb
FabricObjectID      : d903e2c6-3141-4cef-bfe1-04616cd43cbb
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}
```

Das erste Befehls-Cmdlet ruft Mithilfe des **Cmdlets "Get-AzureSiteRecoveryServer"** Server für den aktuellen Azure Site Recovery Vault ab.
Der Befehl speichert die Websitewiederherstellungsserver in $Servers Arrayvariablen.

Der zweite Befehl ruft das Websitewiederherstellungsnetzwerk für den ersten Server im Array $Servers ab.

## PARAMETERS

### -Profile
Gibt das Azure-Profil an, aus dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Server
Gibt einen Websitewiederherstellungsserver an.

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

## AUSGABEN

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN




