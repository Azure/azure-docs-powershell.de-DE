---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: add399ca208cdcd1f1b4395523f8df43875ff451
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303027"
---
# <span data-ttu-id="d674c-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d674c-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="d674c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d674c-102">SYNOPSIS</span></span>
<span data-ttu-id="d674c-103">Mit diesem Befehl werden alle geschützten Elemente in einem bestimmten Container oder über alle registrierten Container hinweg abgerufen.</span><span class="sxs-lookup"><span data-stu-id="d674c-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="d674c-104">Sie besteht aus allen Elementen der Hierarchie der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d674c-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="d674c-105">Gibt "DBs" und deren Entitäten der oberen Ebene zurück, z. B. "Instance", "AvailabilityGroup" usw.</span><span class="sxs-lookup"><span data-stu-id="d674c-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="d674c-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d674c-106">SYNTAX</span></span>

### <span data-ttu-id="d674c-107">NoFilterParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d674c-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d674c-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="d674c-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d674c-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="d674c-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d674c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d674c-110">DESCRIPTION</span></span>
<span data-ttu-id="d674c-111">Das **Cmdlet "Get-AzRecoveryServicesBackupProtectableItem"** ruft die Liste der geschützten Elemente in einem Container und den Schutzstatus der Elemente ab.</span><span class="sxs-lookup"><span data-stu-id="d674c-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="d674c-112">Ein Container, der in einem Azure Recovery Services-Tresor registriert ist, kann ein oder mehrere Elemente enthalten, die geschützt werden können.</span><span class="sxs-lookup"><span data-stu-id="d674c-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="d674c-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d674c-113">EXAMPLES</span></span>

### <span data-ttu-id="d674c-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d674c-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="d674c-115">Der erste Befehl ruft den Container vom Typ "MSSQL" ab und speichert ihn dann in der $Container Variable.</span><span class="sxs-lookup"><span data-stu-id="d674c-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="d674c-116">Der zweite Befehl ruft das sicherungsfähige Element in $Container und speichert es dann in der $Item Variable.</span><span class="sxs-lookup"><span data-stu-id="d674c-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="d674c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d674c-117">PARAMETERS</span></span>

### <span data-ttu-id="d674c-118">-Container</span><span class="sxs-lookup"><span data-stu-id="d674c-118">-Container</span></span>
<span data-ttu-id="d674c-119">Container, in dem sich das Element befindet</span><span class="sxs-lookup"><span data-stu-id="d674c-119">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d674c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d674c-120">-DefaultProfile</span></span>
<span data-ttu-id="d674c-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d674c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d674c-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="d674c-122">-ItemType</span></span>
<span data-ttu-id="d674c-123">Gibt den Typ des schützenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="d674c-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="d674c-124">Anwendbare Werte: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span><span class="sxs-lookup"><span data-stu-id="d674c-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemType
Parameter Sets: FilterParamSet, IdParamSet
Aliases:
Accepted values: SQLDataBase, SQLInstance, SQLAvailabilityGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d674c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d674c-125">-Name</span></span>
<span data-ttu-id="d674c-126">Gibt den Namen der Datenbank, Instanz oder Verfügbarkeitsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="d674c-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d674c-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="d674c-127">-ParentID</span></span>
<span data-ttu-id="d674c-128">Die ARM einer Instanz oder AG angegeben.</span><span class="sxs-lookup"><span data-stu-id="d674c-128">Specified the ARM ID of an Instance or AG.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d674c-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d674c-129">-ServerName</span></span>
<span data-ttu-id="d674c-130">Gibt den Namen des Servers an, zu dem das Element gehört.</span><span class="sxs-lookup"><span data-stu-id="d674c-130">Specifies the name of the server to which the item belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d674c-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d674c-131">-VaultId</span></span>
<span data-ttu-id="d674c-132">ARM-ID des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="d674c-132">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d674c-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d674c-133">-WorkloadType</span></span>
<span data-ttu-id="d674c-134">Arbeitsauslastungstyp der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d674c-134">Workload type of the resource.</span></span> <span data-ttu-id="d674c-135">Die aktuell unterstützten Werte sind AzureVM, WindowsServer, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="d674c-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, WindowsServer, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d674c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d674c-136">CommonParameters</span></span>
<span data-ttu-id="d674c-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d674c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d674c-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d674c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d674c-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d674c-139">INPUTS</span></span>

### <span data-ttu-id="d674c-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="d674c-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="d674c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d674c-141">System.String</span></span>

## <span data-ttu-id="d674c-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d674c-142">OUTPUTS</span></span>

### <span data-ttu-id="d674c-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="d674c-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="d674c-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d674c-144">NOTES</span></span>

## <span data-ttu-id="d674c-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d674c-145">RELATED LINKS</span></span>
