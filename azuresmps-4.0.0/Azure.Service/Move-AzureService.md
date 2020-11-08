---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8418A93-8E6B-4A1C-B319-7CACE95AB600
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1daf0cb8881beeb71f0b3fe68732d596c56ce12
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006446"
---
# Move-AzureService

## Synopsis
Migriert einen clouddienst zum Azure Resource Manager-Stapel.

## Syntax

### AbortMigrationParameterSet
```
Move-AzureService [-Abort] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### CommitMigrationParameterSet
```
Move-AzureService [-Commit] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PrepareNewMigrationParameterSet
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### PrepareExistingMigrationParameterSet
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### ValidateNewMigrationParameterSet
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### ValidateExistingMigrationParameterSet
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Move-AzureService** migriert einen clouddienst und eine Bereitstellung innerhalb dieses Diensts zu einer Ressourcengruppe im Azure Resource Manager-Stapel.

## Beispiele

### Beispiel 1: Vorbereiten der Dienst Migration
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

Dieser Befehl bereitet den Dienst mit dem Namen "ContosoService" für die Migration auf den Azure Resource Manager-Stapel vor.
Die Migration umfasst die Bereitstellung mit dem Namen ContosoVM.

### Beispiel 2: Starten der Dienst Migration
```
PS C:\> Move-AzureService -Commit -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

Mit diesem Befehl wird die Migration des Diensts mit dem Namen ContosoService zum Azure Resource Manager-Stapel gestartet.
Die Migration umfasst die Bereitstellung mit dem Namen ContosoVM.

### Beispiel 3: Abbrechen der Dienst Migration
```
PS C:\> Move-AzureService -Abort -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

Mit diesem Befehl wird die Migration des Diensts mit dem Namen ContosoService zum Azure Resource Manager-Stapel abgebrochen.

### Beispiel 4: Vorbereiten der Dienst Migration auf ein vorhandenes virtuelles Netzwerk
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "VnetRG" -VirtualNetworkName "ContosoVNET" -SubnetName "ContosoSubnet"
```

Dieser Befehl bereitet den Dienst mit dem Namen "ContosoService" für die Migration auf den Azure Resource Manager-Stapel vor.
Die Migration umfasst die Bereitstellung mit dem Namen ContosoVM.
Bei der Migration wird ein zuvor erstelltes virtuelles Netzwerk verwendet.

### Beispiel 5: Überprüfen der Dienst Migration
```
PS C:\> Move-AzureService -Validate -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

Mit diesem Befehl wird die Migration für den Dienst mit dem Namen ContosoService zum Azure Resource Manager-Stapel überprüft.
Die Migration umfasst die Bereitstellung mit dem Namen ContosoVM.

### Beispiel 6: Überprüfen der Dienst Migration zu einem vorhandenen virtuellen Netzwerk
```
PS C:\> Move-AzureService -Validate -ServiceName "contosoService" -DeploymentName "contosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "vnetRG" -VirtualNetworkName "contosoVNET" -SubnetName "contosoSubnet"
```

Mit diesem Befehl wird die Migration für den Dienst mit dem Namen ContosoService zum Azure Resource Manager-Stapel überprüft.
Die Migration umfasst die Bereitstellung mit dem Namen ContosoVM.
Bei der Migration wird ein zuvor erstelltes virtuelles Netzwerk verwendet.

## Parameter

### -Abort
Gibt an, dass dieses Cmdlet die Dienst Migration abbricht.

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Commit
Gibt an, dass dieses Cmdlet die Dienst Migration startet.

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreateNewVirtualNetwork
Gibt an, dass dieses Cmdlet im Azure Resource Manager-Stapel ein virtuelles Netzwerk erstellt.

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, ValidateNewMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Deploymentname
Gibt den Namen der Cloud-Dienstbereitstellung an, die dieses Cmdlet migriert.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
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

### -Vorbereiten
Gibt an, dass dieses Cmdlet den cloudbasierten Dienst für die Migration vorbereitet.

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, PrepareExistingMigrationParameterSet
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

### -ServiceName
Gibt den Namen des Cloud-Diensts an, den dieses Cmdlet migriert.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetName
Gibt den Namen des Subnets im virtuellen Netzwerk an.

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseExistingVirtualNetwork
Gibt an, dass dieses Cmdlet den cloudbasierten Dienst in ein vorhandenes virtuelles Netzwerk im Azure Resource Manager-Stapel migriert.

```yaml
Type: SwitchParameter
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Validate
Gibt an, dass dieses Cmdlet den cloudbasierten Dienst für die Migration überprüft.

```yaml
Type: SwitchParameter
Parameter Sets: ValidateNewMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkName
Gibt den Namen eines virtuellen Netzwerks an.

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkResourceGroupName
Gibt den Namen der Ressourcengruppe eines vorhandenen virtuellen Netzwerks an.

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Verschieben-AzureNetworkSecurityGroup](./Move-AzureNetworkSecurityGroup.md)

[Verschieben-AzureReservedIP](./Move-AzureReservedIP.md)

[Verschieben-AzureRouteTable](./Move-AzureRouteTable.md)

[Verschieben-AzureStorageAccount](./Move-AzureStorageAccount.md)

[Verschieben-AzureVirtualNetwork](./Move-AzureVirtualNetwork.md)


