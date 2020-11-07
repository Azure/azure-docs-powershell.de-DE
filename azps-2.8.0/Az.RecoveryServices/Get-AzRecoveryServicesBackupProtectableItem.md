---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 03e990f36c8846ad1055d5d2f8873ead18536128
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824336"
---
# <span data-ttu-id="2252b-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2252b-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="2252b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2252b-102">SYNOPSIS</span></span>
<span data-ttu-id="2252b-103">Dieser Befehl ruft alle geschützten Elemente innerhalb eines bestimmten Containers oder in allen registrierten Containern ab.</span><span class="sxs-lookup"><span data-stu-id="2252b-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="2252b-104">Sie wird aus allen Elementen der Hierarchie der Anwendung bestehen.</span><span class="sxs-lookup"><span data-stu-id="2252b-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="2252b-105">Gibt DBS und deren Entitäten der obersten Ebene wie instance, availabilitygroup usw. zurück.</span><span class="sxs-lookup"><span data-stu-id="2252b-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="2252b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2252b-106">SYNTAX</span></span>

### <span data-ttu-id="2252b-107">NoFilterParamSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2252b-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2252b-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="2252b-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2252b-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="2252b-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2252b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2252b-110">DESCRIPTION</span></span>
<span data-ttu-id="2252b-111">Mit dem Cmdlet **Get-AzRecoveryServicesBackupProtectableItem werden** die geschützten Elemente in einem Container oder ein Wert in Azure Backup und der Schutzstatus der Elemente abgerufen.</span><span class="sxs-lookup"><span data-stu-id="2252b-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the protectable items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="2252b-112">Ein Container, der in einem Azure Recovery Services Vault registriert ist, kann ein oder mehrere Elemente enthalten, die geschützt werden können.</span><span class="sxs-lookup"><span data-stu-id="2252b-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="2252b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2252b-113">EXAMPLES</span></span>

### <span data-ttu-id="2252b-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2252b-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="2252b-115">Der erste Befehl ruft den Container des Typs MSSQL ab und speichert ihn dann in der $Container-Variablen.</span><span class="sxs-lookup"><span data-stu-id="2252b-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="2252b-116">Der zweite Befehl ruft das Sicherungselement in $Container ab und speichert es dann in der $Item Variablen.</span><span class="sxs-lookup"><span data-stu-id="2252b-116">The second command gets the Backup item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="2252b-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="2252b-117">PARAMETERS</span></span>

### <span data-ttu-id="2252b-118">-Container</span><span class="sxs-lookup"><span data-stu-id="2252b-118">-Container</span></span>
<span data-ttu-id="2252b-119">Container, in dem sich das Element befindet</span><span class="sxs-lookup"><span data-stu-id="2252b-119">Container where the item resides</span></span>

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

### <span data-ttu-id="2252b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2252b-120">-DefaultProfile</span></span>
<span data-ttu-id="2252b-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2252b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2252b-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="2252b-122">-ItemType</span></span>
<span data-ttu-id="2252b-123">Gibt den Typ des geschützten Elements an.</span><span class="sxs-lookup"><span data-stu-id="2252b-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="2252b-124">Anwendbare Werte: (SQLDatabase, SQLInstance, sqlavailabilitygroup).</span><span class="sxs-lookup"><span data-stu-id="2252b-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

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

### <span data-ttu-id="2252b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2252b-125">-Name</span></span>
<span data-ttu-id="2252b-126">Gibt den Namen der Datenbank, der Instanz oder der Verfügbarkeits Kategorie an.</span><span class="sxs-lookup"><span data-stu-id="2252b-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

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

### <span data-ttu-id="2252b-127">-Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="2252b-127">-ParentID</span></span>
<span data-ttu-id="2252b-128">Die Arm-ID einer Instanz oder AG angegeben.</span><span class="sxs-lookup"><span data-stu-id="2252b-128">Specified the ARM ID of an Instance or AG.</span></span>

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

### <span data-ttu-id="2252b-129">-Servername</span><span class="sxs-lookup"><span data-stu-id="2252b-129">-ServerName</span></span>
<span data-ttu-id="2252b-130">Gibt den Namen des Servers an, zu dem das Element gehört.</span><span class="sxs-lookup"><span data-stu-id="2252b-130">Specifies the name of the server to which the item belongs.</span></span>

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

### <span data-ttu-id="2252b-131">-Tresor</span><span class="sxs-lookup"><span data-stu-id="2252b-131">-VaultId</span></span>
<span data-ttu-id="2252b-132">Arm-ID des Speichers für Wiederherstellungsdienste</span><span class="sxs-lookup"><span data-stu-id="2252b-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2252b-133">-Workloadtype</span><span class="sxs-lookup"><span data-stu-id="2252b-133">-WorkloadType</span></span>
<span data-ttu-id="2252b-134">Arbeits Auslastungs der Ressource (Beispiel: AzureVM, Windows Server, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="2252b-134">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2252b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2252b-135">CommonParameters</span></span>
<span data-ttu-id="2252b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2252b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2252b-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2252b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2252b-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2252b-138">INPUTS</span></span>

### <span data-ttu-id="2252b-139">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="2252b-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="2252b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2252b-140">System.String</span></span>

## <span data-ttu-id="2252b-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2252b-141">OUTPUTS</span></span>

### <span data-ttu-id="2252b-142">Microsoft. Azure. Commands. RecoveryServices. Backup. Cmdlets. Models. ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="2252b-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="2252b-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="2252b-143">NOTES</span></span>

## <span data-ttu-id="2252b-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2252b-144">RELATED LINKS</span></span>