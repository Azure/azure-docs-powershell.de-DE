---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006263"
---
# Set-AzureEndpoint

## Synopsis
Ändert einen Endpunkt, der einem virtuellen Computer zugewiesen ist.

## Syntax

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureEndpoint** " ändert einen Endpunkt, der einem Azure Virtual Machine zugewiesen ist.
Sie können Änderungen an einem Endpunkt angeben, bei dem es sich nicht um einen Lastenausgleich handelt.

## Beispiele

### Beispiel 1: Ändern eines Endpunkts, um einen Port zu überwachen
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

Dieser Befehl ruft mit dem Cmdlet **Get-AzureVM** die Konfiguration eines virtuellen Computers mit dem Namen VirtualMachine01 ab.
Der Befehl übergibt ihn mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Mit diesem Cmdlet wird der Endpunkt mit dem Namen Web so geändert, dass er Port 443 überwacht.
Der Befehl übergibt das Objekt des virtuellen Computers an das Cmdlet **Update-AzureVM** , das Ihre Änderungen implementiert.

## Parameter

### -ACL
Gibt ein Configuration-Objekt für die Zugriffssteuerungsliste (ACL) an, das dieses Cmdlet auf den Endpunkt anwendet.

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DirectServerReturn
Gibt an, ob dieses Cmdlet die direkte Server Rückgabe ermöglicht.
Geben Sie $true an, die aktiviert werden soll, oder deaktivieren Sie $false.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
Gibt den TCP-Leerlauftimeout Zeitraum (in Minuten) für den Endpunkt an.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Information
Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Weiterhin
- Ignorieren
- Erkundigen
- SilentlyContinue
- Beenden
- Anhalten

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Gibt eine Informations Variable an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InternalLoadBalancerName
Gibt den Namen des internen Lastenausgleichs an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoadBalancerDistribution
Gibt den Verteilungs Algorithmus des Lastenausgleichs an.
Gültige Werte sind: 

- sourceIP.
Zwei Tupel-Affinität: Quell-IP, Ziel-IP 
- sourceIPProtocol.
Eine drei-Tupel-Affinität: Quell-IP, Ziel-IP, Protokoll 
- keine.
Eine fünf-Tupel-Affinität: Quell-IP, Quell-Port, Ziel-IP, Ziel-Port, Protokoll 

Der Standardwert ist None.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalPort
Gibt den lokalen, privaten Port an, den dieser Endpunkt verwendet.
Anwendungen innerhalb des virtuellen Computers lauschen diesem Port für Dienst Eingabeanforderungen für diesen Endpunkt.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des Endpunkts an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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

### -Protokoll
Gibt das Protokoll des Endpunkts an.
Gültige Werte sind: 

- TCP 
- UDP

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

### -PublicPort
Gibt den öffentlichen Port an, den der Endpunkt verwendet.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualIPName
Gibt den Namen einer virtuellen IP-Adresse an, die Azure dem Endpunkt zuordnet.
Ihr Dienst kann mehrere virtuelle IPS aufweisen.
Verwenden Sie zum Erstellen von virtuellen IPS das Cmdlet **Add-AzureVirtualIP** .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Gibt den virtuellen Computer an, zu dem der Endpunkt gehört.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### System. Object

## Notizen

## Verwandte Links

[Add-AzureEndpoint](./Add-AzureEndpoint.md)

[Add-AzureVirtualIP](./Add-AzureVirtualIP.md)

[Get-AzureEndpoint](./Get-AzureEndpoint.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureEndpoint](./Remove-AzureEndpoint.md)

[Update-AzureVM](./Update-AzureVM.md)


