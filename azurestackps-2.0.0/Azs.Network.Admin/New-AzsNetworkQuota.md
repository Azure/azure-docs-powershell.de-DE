---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/new-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: 554ebe0e6c4ef8a4b0d262071595c0dc6336f482
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842528"
---
# New-AzsNetworkQuota

## Synopsis
Erstellen oder Aktualisieren eines Kontingents

## Syntax

### Createexpanded (Standard)
```
New-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-MaxLoadBalancersPerSubscription <Int64>] [-MaxNicsPerSubscription <Int64>]
 [-MaxPublicIpsPerSubscription <Int64>] [-MaxSecurityGroupsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Erstellen
```
New-AzsNetworkQuota -Name <String> -Quota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CreateViaIdentity
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> -Quota <IQuota> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### CreateViaIdentityExpanded
```
New-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-MaxLoadBalancersPerSubscription <Int64>]
 [-MaxNicsPerSubscription <Int64>] [-MaxPublicIpsPerSubscription <Int64>]
 [-MaxSecurityGroupsPerSubscription <Int64>] [-MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64>]
 [-MaxVirtualNetworkGatewaysPerSubscription <Int64>] [-MaxVnetsPerSubscription <Int64>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Beschreibung
Erstellen oder Aktualisieren eines Kontingents

## Beispiele

### --------------------------Beispiel 1--------------------------
```
New-AzsNetworkQuota -Name NetworkQuotaDefaultValues
```

Erstellen Sie ein neues Netzwerk Kontingent mit allen Standardwerten.

### --------------------------Beispiel 2--------------------------
```
New-AzsNetworkQuota -Name NetworkQuota1 -MaxNicsPerSubscription 150 -MaxPublicIpsPerSubscription 150
```
Erstellen Sie ein neues Netzwerk Kontingent mit nicht Standardwerten für Kontingent.



## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Inputobject
Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Standort
Der Speicherort der Ressource.

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxLoadBalancersPerSubscription
Die maximale Anzahl von Last-Balancern, die ein Mandanten Abonnement bereitstellen kann.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxNicsPerSubscription
Die maximale Anzahl von NICs, die ein Mandanten Abonnement bereitstellen kann.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxPublicIpsPerSubscription
Die maximale Anzahl von öffentlichen IP-Adressen, die ein Mandanten Abonnement bereitstellen kann.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxSecurityGroupsPerSubscription
Die maximale Anzahl von Sicherheitsgruppen, die ein Mandanten Abonnement bereitstellen kann.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVirtualNetworkGatewayConnectionsPerSubscription
Maximale Anzahl von virtuellen Netzwerk-Gateway-Verbindungen, die ein Mandanten Abonnement bereitstellen kann.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVirtualNetworkGatewaysPerSubscription
Maximale Anzahl von virtuellen Netzwerkgateways, die ein Mandanten Abonnement bereitstellen kann.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False

```

### -MaxVnetsPerSubscription
Die maximale Anzahl von virtuellen Netzwerken, die ein Mandanten Abonnement bereitstellen kann.

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: 50
Accept pipeline input: False
Accept wildcard characters: False

```

### -Name
Der Name der Ressource.

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Kontingent
Netzwerk Kontingent Ressource
Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Kontingenteigenschaften und Erstellen einer Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Abonnement-Nr
Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.
Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### -Tag
Liste der Schlüssel-Wert-Paare

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Bestätigen
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

### -WhatIf
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IQuota

### Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. INetworkAdminIdentity

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. NetworkAdmin. Models. Api20150615. IQuota



## Notizen

Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.

Inputobject <INetworkAdminIdentity> : Identity-Parameter
  - `[Id <String>]`: Ressourcen Identitäts Pfad
  - `[Location <String>]`: Speicherort der Ressource.
  - `[ResourceName <String>]`: Name der Ressource.
  - `[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.

Kontingent <IQuota> : Netzwerk Kontingent Ressource.
  - `[Tag <IResourceTags>]`: Liste von Schlüsselwert-Paaren.
    - `[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.
  - `[MaxLoadBalancersPerSubscription <Int64?>]`: Maximale Anzahl von Last-Balancern, die ein Mandanten Abonnement bereitstellen kann.
  - `[MaxNicsPerSubscription <Int64?>]`: Maximale Anzahl von NICs, die ein Mandanten Abonnement bereitstellen kann.
  - `[MaxPublicIpsPerSubscription <Int64?>]`: Maximale Anzahl von öffentlichen IP-Adressen, die ein Mandanten Abonnement bereitstellen kann.
  - `[MaxSecurityGroupsPerSubscription <Int64?>]`: Maximale Anzahl von Sicherheitsgruppen, die ein Mandanten Abonnement bereitstellen kann.
  - `[MaxVirtualNetworkGatewayConnectionsPerSubscription <Int64?>]`: Maximale Anzahl von virtuellen Netzwerk-Gateway-Verbindungen, die ein Mandanten Abonnement bereitstellen kann.
  - `[MaxVirtualNetworkGatewaysPerSubscription <Int64?>]`: Maximale Anzahl von virtuellen Netzwerkgateways, die ein Mandanten Abonnement bereitstellen kann.
  - `[MaxVnetsPerSubscription <Int64?>]`: Maximale Anzahl von virtuellen Netzwerken, die ein Mandanten Abonnement bereitstellen kann.

## Verwandte Links

