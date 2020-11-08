---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 2021B6BC-7B59-4A88-B1DF-598203F58901
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e225702238f9a90891db819753a68f728a482f9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006202"
---
# New-AzureRemoteAppCollection

## Synopsis
Erstellt eine Azure RemoteApp-Sammlung.

## Syntax

### AllParameterSets (Standard)
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-Description <String>] [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### AzureVNet
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-VNetName] <String> [-SubnetName] <String> [-DnsServers <String>] [[-Domain] <String>]
 [[-Credential] <PSCredential>] [-OrganizationalUnit <String>] [-Description <String>]
 [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRemoteAppCollection** erstellt eine Azure RemoteApp-Sammlung.

## Beispiele

### Beispiel 1: Erstellen einer Sammlung
```
PS C:\> New-AzureRemoteAppCollection -CollectionName "Contoso" -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
```

Dieser Befehl erstellt eine Azure RemoteApp-Sammlung.

### Beispiel 2: Erstellen einer Sammlung mithilfe von Anmeldeinformationen
```
PS C:\> $cred = Get-Credential corp.contoso.com\admin
PS C:\> New-AzureRemoteAppCollection -CollectionName "ContosoHybrid" -ImageName "Windows Server 2012 R2" -Plan Standard -VNetName azureVNet -Domain Contoso.com -Credential $cred -Description Hybrid
```

Dieser Befehl erstellt eine Azure RemoteApp-Sammlung unter Verwendung einer Anmeldeinformationen aus dem Cmdlet **Get-Credential** .

## Parameter

### -CollectionName
Gibt den Namen der Azure RemoteApp-Sammlung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### – Anmeldeinformationen
Gibt die Anmeldeinformationen eines Dienstkontos an, das über die Berechtigung zum beitreten der Azure RemoteApp-Server zu Ihrer Domäne verfügt.
Verwenden Sie das Cmdlet **Get-Credential** , um ein **PSCredential** -Objekt zu erhalten.

```yaml
Type: PSCredential
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomRdpProperty
Gibt benutzerdefinierte Remote Desktop-Eigenschaften an, die zum Konfigurieren der Laufwerkumleitung und anderer Einstellungen verwendet werden können.
Details finden Sie unter [RDP-Einstellungen für Remote Desktop Dienste in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Beschreibung
Gibt eine kurze Beschreibung für das Objekt an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DnsServers
Gibt eine durch trennzeichengetrennte Liste der IPv4-Adressen der DNS-Server an.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Domäne
Gibt den Namen der Active Directory-Domänendienst Domäne an, an die die Server mit dem Host für Remotedesktopsitzungen teilnehmen sollen.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bildname
Gibt den Namen des Azure RemoteApp-Vorlagenbilds an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Standort
Gibt den Azure-Bereich der Sammlung an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrganizationalUnit
Gibt den Namen der Organisationseinheit an, an die die Hostserver für Remotedesktopsitzungen teilnehmen sollen, beispielsweise ou = MyOu, DC = MyDomain, DC = ParentDomain, DC = com.
Attribute wie ou und DC müssen in Großbuchstaben eingegeben werden.
Die OU kann nach der Erstellung der Sammlung nicht mehr geändert werden.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plan
Gibt den Plan für die Azure RemoteApp-Sammlung an, die die Nutzungs Grenzwerte definieren kann.
Verwenden Sie " **Get-AzureRemoteAppPlan** ", um die verfügbaren Pläne anzuzeigen.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
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

### -
Gibt den Ressourcentyp der Sammlung an.
Die akzeptablen Werte für diesen Parameter sind: App oder Desktop.

```yaml
Type: CollectionMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetName
Gibt den Namen des Subnets im virtuellen Netzwerk an, das zum Erstellen der Azure RemoteApp-Sammlung verwendet werden soll.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VNetName
Gibt den Namen eines virtuellen Azure RemoteApp-Netzwerks an.

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[Get-AzureRemoteAppPlan](./Get-AzureRemoteAppPlan.md)

[Remove-AzureRemoteAppCollection](./Remove-AzureRemoteAppCollection.md)

[Satz-AzureRemoteAppCollection](./Set-AzureRemoteAppCollection.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


