---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsvolume
schema: 2.0.0
ms.openlocfilehash: a423470454e77c58a8b611a47c737e5d86bfd1cf
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005510"
---
# Get-AzsVolume

## Synopsis
Geben Sie das angeforderte Speichervolumen zurück.

## Syntax

### Liste (Standard)
```
Get-AzsVolume -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### Erhalten
```
Get-AzsVolume -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsVolume -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## Beschreibung
Geben Sie das angeforderte Speichervolumen zurück.

## Beispiele

### Beispiel 1:
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsVolume -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

Sie erhalten eine Liste aller Speicher-Volumes an einem bestimmten Ort.

### Beispiel 2:
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsVolume -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name ee594cf5-cf54-46b4-a641-139553307195
```

Besorgen Sie sich ein Speichervolumen nach Name an einem bestimmten Ort.

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
Name des Speicher Datenträgers.

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

### -ScaleUnit
Name der Skalierungseinheiten

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Skip
OData-Skip-Parameter

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

### -StorageSubSystem
Name des Speichersystems

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
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

### -Top
OData-oberer Parameter.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20190501. IVolume



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
  - `[StorageSubSystem <String>]`: Name des Speichersystems.
  - `[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.
  - `[Volume <String>]`: Name des Speicher Datenträgers.

## Verwandte Links

