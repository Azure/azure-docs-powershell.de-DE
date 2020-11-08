---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: add399ca208cdcd1f1b4395523f8df43875ff451
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173111"
---
# <span data-ttu-id="e5d1d-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="e5d1d-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="e5d1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d1d-103">Dieser Befehl ruft alle geschützten Elemente innerhalb eines bestimmten Containers oder in allen registrierten Containern ab.</span><span class="sxs-lookup"><span data-stu-id="e5d1d-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="e5d1d-104">Sie wird aus allen Elementen der Hierarchie der Anwendung bestehen.</span><span class="sxs-lookup"><span data-stu-id="e5d1d-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="e5d1d-105">Gibt DBS und deren Entitäten der obersten Ebene wie instance, availabilitygroup usw. zurück.</span><span class="sxs-lookup"><span data-stu-id="e5d1d-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="e5d1d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5d1d-106">SYNTAX</span></span>

### <span data-ttu-id="e5d1d-107">NoFilterParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5d1d-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5d1d-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="e5d1d-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5d1d-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="e5d1d-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5d1d-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5d1d-110">DESCRIPTION</span></span>
<span data-ttu-id="e5d1d-111">Das Cmdlet " **Get-AzRecoveryServicesBackupProtectableItem** " Ruft die Liste der geschützten Elemente in einem Container und den Schutzstatus der Elemente ab.</span><span class="sxs-lookup"><span data-stu-id="e5d1d-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="e5d1d-112">Ein Container, der in einem Azure Recovery Services Vault registriert ist, kann ein oder mehrere Elemente enthalten, die geschützt werden können.</span><span class="sxs-lookup"><span data-stu-id="e5d1d-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="e5d1d-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5d1d-113">EXAMPLES</span></span>

### <span data-ttu-id="e5d1d-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5d1d-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="e5d1d-115">Der erste Befehl ruft den Container des Typs MSSQL ab und speichert ihn dann in der $Container-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e5d1d-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="e5d1d-116">Der zweite Befehl ruft das zu schützende Sicherungselement in $Container ab und speichert es dann in der $Item-Variablen.</span><span class="sxs-lookup"><span data-stu-id="e5d1d-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="e5d1d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5d1d-117">PARAMETERS</span></span>

### <span data-ttu-id="e5d1d-118">-Container</span><span class="sxs-lookup"><span data-stu-id="e5d1d-118">-Container</span></span>
<span data-ttu-id="e5d1d-119">Container, in dem sich das Element befindet</span><span class="sxs-lookup"><span data-stu-id="e5d1d-119">Container where the item resides</span></span>

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

### <span data-ttu-id="e5d1d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d1d-120">-DefaultProfile</span></span>
<span data-ttu-id="e5d1d-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5d1d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5d1d-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="e5d1d-122">-ItemType</span></span>
<span data-ttu-id="e5d1d-123">Gibt den Typ des geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="e5d1d-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="e5d1d-124">Anwendbare Werte: (SQLDatabase, SQLInstance, sqlavailabilitygroup).</span><span class="sxs-lookup"><span data-stu-id="e5d1d-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

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

### <span data-ttu-id="e5d1d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e5d1d-125">-Name</span></span>
<span data-ttu-id="e5d1d-126">Gibt den Namen der Datenbank, der Instanz oder der Verfügbarkeits Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="e5d1d-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

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

### <span data-ttu-id="e5d1d-127">-Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5d1d-127">-ParentID</span></span>
<span data-ttu-id="e5d1d-128">Die Arm-ID einer Instanz oder AG angegeben.</span><span class="sxs-lookup"><span data-stu-id="e5d1d-128">Specified the ARM ID of an Instance or AG.</span></span>

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

### <span data-ttu-id="e5d1d-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="e5d1d-129">-ServerName</span></span>
<span data-ttu-id="e5d1d-130">Gibt den Namen des Servers an, zu dem das Element gehört.</span><span class="sxs-lookup"><span data-stu-id="e5d1d-130">Specifies the name of the server to which the item belongs.</span></span>

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

### <span data-ttu-id="e5d1d-131">-Tresor</span><span class="sxs-lookup"><span data-stu-id="e5d1d-131">-VaultId</span></span>
<span data-ttu-id="e5d1d-132">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="e5d1d-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e5d1d-133">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="e5d1d-133">-WorkloadType</span></span>
<span data-ttu-id="e5d1d-134">Arbeits Auslastungs der Ressource.</span><span class="sxs-lookup"><span data-stu-id="e5d1d-134">Workload type of the resource.</span></span> <span data-ttu-id="e5d1d-135">Die aktuell unterstützten Werte sind AzureVM, Windows Server, AzureFiles, MSSQL</span><span class="sxs-lookup"><span data-stu-id="e5d1d-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="e5d1d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d1d-136">CommonParameters</span></span>
<span data-ttu-id="e5d1d-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5d1d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d1d-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5d1d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d1d-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5d1d-139">INPUTS</span></span>

### <span data-ttu-id="e5d1d-140">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="e5d1d-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="e5d1d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e5d1d-141">System.String</span></span>

## <span data-ttu-id="e5d1d-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5d1d-142">OUTPUTS</span></span>

### <span data-ttu-id="e5d1d-143">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="e5d1d-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="e5d1d-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5d1d-144">NOTES</span></span>

## <span data-ttu-id="e5d1d-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5d1d-145">RELATED LINKS</span></span>
