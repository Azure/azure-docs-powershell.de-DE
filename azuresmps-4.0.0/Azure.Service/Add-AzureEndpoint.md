---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D767F017-6545-4BC6-927E-E7A99A08D5D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b3122795f2af33a28206936b7b28322ad171b19
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005939"
---
# Add-AzureEndpoint

## Synopsis
Fügt einen Endpunkt zu einem virtuellen Computer hinzu.

## Syntax

### NoLB (Standard)
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### LBNoProbe
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-NoProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### LBDefaultProbe
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-DefaultProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### LBCustomProbe
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> -ProbePort <Int32>
 -ProbeProtocol <String> [-ProbePath <String>] [-ProbeIntervalInSeconds <Int32>]
 [-ProbeTimeoutInSeconds <Int32>] [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadBalancerDistribution <String>] [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **Add-AzureEndpoint** wird ein Endpunkt zu einem Azure Virtual Machine-Objekt hinzugefügt.

## Beispiele

### Beispiel 1: Hinzufügen eines Endpunkts
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 | Update-AzureVM
```

Dieser Befehl ruft mit dem Cmdlet **Get-AzureVM** die Konfiguration eines virtuellen Computers mit dem Namen VirtualMachine01 ab.
Der Befehl übergibt ihn mithilfe des Pipelineoperators an das aktuelle Cmdlet.
Mit diesem Cmdlet wird ein Endpunkt mit dem Namen httpin hinzugefügt.
Der Endpunkt verfügt über einen öffentlichen Port 80 und einen lokalen Port 8080.
Der Befehl übergibt das Objekt des virtuellen Computers an das Cmdlet **Update-AzureVM** , das Ihre Änderungen implementiert.

### Beispiel 2: Hinzufügen eines Endpunkts, der zu einer Lastenausgleichs Gruppe gehört
```
PS C:\> Get-AzureVM -ServiceName "LoadBalancedService" -Name "VirtualMachine12" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 -LBSetName "WebFarm" -ProbePort 80 -ProbeProtocol "http" -ProbePath '/' | Update-AzureVM
```

Dieser Befehl ruft die Konfiguration eines virtuellen Computers mit dem Namen VirtualMachine07 ab.
Das aktuelle Cmdlet fügt einen Endpunkt mit dem Namen httpin hinzu.
Der Endpunkt verfügt über einen öffentlichen Port 80 und einen lokalen Port 8080.
Der Endpunkt gehört zur Gruppe Shared Load Balanced mit dem Namen Webfarm.
Eine HTTP-Sonde auf Port 80 mit dem Pfad "/" überwacht die Verfügbarkeit des Endpunkts.
Der Befehl implementiert Ihre Änderungen.

### Beispiel 3: Zuordnen einer virtuellen IP zu einem Endpunkt
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine25" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -LocalPort 8080 -PublicPort 80 -VirtualIPName "ContosoVip11" | Update-AzureVM
```

Dieser Befehl ruft die Konfiguration eines virtuellen Computers mit dem Namen VirtualMachine25 ab.
Das aktuelle Cmdlet fügt einen Endpunkt mit dem Namen httpin hinzu.
Der Endpunkt verfügt über einen öffentlichen Port 80 und einen lokalen Port 8080.
Dieser Befehl ordnet dem Endpunkt eine virtuelle IP-Adresse zu.
Der Befehl implementiert Ihre Änderungen.

## Parameter

### -ACL
Gibt ein Configuration-Objekt für die Zugriffssteuerungsliste (ACL) für den Endpunkt an.

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

### -DefaultProbe
Gibt an, dass dieses Cmdlet die standardmäßige Prüf Punkt Einstellung verwendet.

```yaml
Type: SwitchParameter
Parameter Sets: LBDefaultProbe
Aliases: 

Required: True
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

### -LBSetName
Gibt den Namen des Load Balancer-Satzes für den Endpunkt an.

```yaml
Type: String
Parameter Sets: LBNoProbe, LBDefaultProbe, LBCustomProbe
Aliases: LoadBalancedEndpointSetName

Required: True
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

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt einen Namen für den Endpunkt an.

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

### -Noprobe
Gibt an, dass dieses Cmdlet die Einstellung keine Sonde verwendet.

```yaml
Type: SwitchParameter
Parameter Sets: LBNoProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeIntervalInSeconds
Gibt das Abfrageintervall für den Prüfpunkt in Sekunden für den Endpunkt an.

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbePath
Gibt den relativen Pfad zur http-Sonde an.

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbePort
Gibt den Port an, den der Endpunkt verwendet.

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeProtocol
Gibt das Port Protokoll an.
Gültige Werte sind: 

- TCP 
- http

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProbeTimeoutInSeconds
Gibt den Zeitüberschreitungszeitraum für das Abrufen von Sonden in Sekunden an.

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
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

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicPort
Gibt den öffentlichen Port an, den der Endpunkt verwendet.
Wenn Sie keinen Wert angeben, weist Azure einen verfügbaren Port zu.

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

[Add-AzureVirtualIP](./Add-AzureVirtualIP.md)

[Get-AzureEndpoint](./Get-AzureEndpoint.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureEndpoint](./Remove-AzureEndpoint.md)

[Satz-AzureEndpoint](./Set-AzureEndpoint.md)

[Update-AzureVM](./Update-AzureVM.md)


