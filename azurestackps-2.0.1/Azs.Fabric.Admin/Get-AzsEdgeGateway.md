---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegateway
schema: 2.0.0
ms.openlocfilehash: a9c883fab422252aad167d92da3adf55edd9a78b
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005562"
---
# Get-AzsEdgeGateway

## Synopsis
Gibt das angeforderte Edge-Gateway zurück.

## Syntax

### Liste (Standard)
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### Erhalten
```
Get-AzsEdgeGateway -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsEdgeGateway -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## Beschreibung
Gibt das angeforderte Edge-Gateway zurück.

## Beispiele

### Beispiel 1:
```powershell
PS C:\> Get-AzsEdgeGateway

Get a list of all edge gateways.
```

Gibt die Liste aller Edge-Gateways an einer bestimmten Position zurück.


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

### -Filter
OData-Filterparameter

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Inputobject
Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
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
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Name
Der Name des Edge-Gateways.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -PassThru
Gibt "true" zurück, wenn der Befehl erfolgreich ist

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -Abonnement-Nr
Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.
Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IEdgeGateway



## Notizen

Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.

Inputobject <IFabricAdminIdentity> : Identity-Parameter
  - `[Drive <String>]`: Name des Speicherlaufwerks.
  - `[EdgeGateway <String>]`: Name des Edge-Gateways.
  - `[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.
  - `[FabricLocation <String>]`: Fabric-Standort.
  - `[FileShare <String>]`: Fabric-Dateifreigabe Name.
  - `[IPPool <String>]`: IP-Pool-Name.
  - `[Id <String>]`: Ressourcen Identitäts Pfad
  - `[InfraRole <String>]`: Name der Infrastruktur Rolle
  - `[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.
  - `[Location <String>]`: Speicherort der Ressource.
  - `[LogicalNetwork <String>]`: Name des logischen Netzwerks.
  - `[LogicalSubnet <String>]`: Name des logischen Subnetzes.
  - `[MacAddressPool <String>]`: Name des Mac-Adresspools.
  - `[Operation <String>]`: Vorgangs-ID.
  - `[ResourceGroupName <String>]`: Name der Ressourcengruppe.
  - `[ScaleUnit <String>]`: Name der Skaleneinheiten.
  - `[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.
  - `[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.
  - `[StoragePool <String>]`: Name des Speicherpools.
  - `[StorageSubSystem <String>]`: Name des Speichersystems.
  - `[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.
  - `[Volume <String>]`: Name des Speicher Datenträgers.

## Verwandte Links

