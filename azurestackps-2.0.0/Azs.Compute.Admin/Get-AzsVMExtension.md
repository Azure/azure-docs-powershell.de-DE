---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsvmextension
schema: 2.0.0
ms.openlocfilehash: c2214f01b35e68ba22f9dbfc6fe9e602badb9ba9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844879"
---
# Get-AzsVMExtension

## Synopsis
Gibt den angeforderten Virtual Machine Extension-Bildabgleich mit Publisher, Typ, Version zurück.

## Syntax

### Liste (Standard)
```
Get-AzsVMExtension [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Erhalten
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Beschreibung
Gibt den angeforderten Virtual Machine Extension-Bildabgleich mit Publisher, Typ, Version zurück.

## Beispiele

### Beispiel 1: Abrufen aller VM-Erweiterungen
```powershell
PS C:\> Get-AzsVMExtension

ExtensionType            : IaaSDiagnostics
TypeHandlerVersion       : 1.11.3.12
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/northwest/artifactTypes/VMExtension/publishers/Microsoft.Azure.Diagnostics/types/IaaSDia
                           gnostics/versions/1.11.3.12
IsSystemExtension        : False
Location                 : northwest
Name                     :
ProvisioningState        : Succeeded
Publisher                : Microsoft.Azure.Diagnostics
SourceBlobUri            :
SupportMultipleExtension : False
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Windows

...
```

Rufen Sie eine Liste aller VMExtensions ab, indem Sie alle Parameter leer lassen.

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
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
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

### -Publisher
Der Name des Herausgebers.

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

### -Typ
Der Typ der Erweiterung.

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

### -Version
Die Version der Ressource.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20151201Preview. IVMExtension



## Notizen

Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.

Inputobject <IComputeAdminIdentity> : Identity-Parameter
  - `[DiskId <String>]`: Die Datenträger-GUID als Identität.
  - `[Id <String>]`: Ressourcen Identitäts Pfad
  - `[Location <String>]`: Speicherort der Ressource.
  - `[MigrationId <String>]`: Der GUID-Name des Migrationsauftrags.
  - `[Offer <String>]`: Name des Angebots.
  - `[Publisher <String>]`: Name des Herausgebers.
  - `[QuotaName <String>]`: Name des Kontingents.
  - `[Sku <String>]`: Name der SKU.
  - `[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.
  - `[Type <String>]`: Typ der Erweiterung.
  - `[Version <String>]`: Die Version der Ressource.

## Verwandte Links

