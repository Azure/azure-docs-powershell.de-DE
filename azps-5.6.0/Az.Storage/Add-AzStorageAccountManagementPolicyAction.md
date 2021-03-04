---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: 65bce04c3df14a6b9dc4397d47577d0642746c45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930707"
---
# <span data-ttu-id="0f406-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="0f406-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="0f406-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f406-102">SYNOPSIS</span></span>
<span data-ttu-id="0f406-103">Fügt dem Input ManagementPolicy Action Group-Objekt eine Aktion hinzu, oder erstellt mit der Aktion ein ManagementPolicy-Aktionsgruppe-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0f406-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="0f406-104">Das -Objekt kann in New-AzStorageAccountManagementPolicyRule verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f406-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="0f406-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f406-105">SYNTAX</span></span>

### <span data-ttu-id="0f406-106">BaseBlob (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f406-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f406-107">Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="0f406-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f406-108">BlobVersion</span><span class="sxs-lookup"><span data-stu-id="0f406-108">BlobVersion</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BlobVersionAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f406-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f406-109">DESCRIPTION</span></span>
<span data-ttu-id="0f406-110">Das **Add-AzStorageAccountManagementPolicyAction-Cmdlet** fügt dem Input ManagementPolicy Action Group-Objekt eine Aktion hinzu, oder erstellt mit der Aktion ein ManagementPolicy-Aktionsgruppe-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0f406-110">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="0f406-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f406-111">EXAMPLES</span></span>

### <span data-ttu-id="0f406-112">Beispiel 1: Erstellt ein ManagementPolicy Action Group-Objekt mit vier Aktionen, fügt es dann einer Verwaltungsrichtlinienregel hinzu und wird auf ein Speicherkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f406-112">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100
Version.TierToCool.DaysAfterCreationGreaterThan         : 
Version.TierToArchive.DaysAfterCreationGreaterThan      : 
Version.Delete.DaysAfterCreationGreaterThan             : 

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="0f406-113">Mit dem ersten Befehl wird ein ManagementPolicy Action Group-Objekt erstellt, mit den folgenden drei Befehlen werden dem Objekt drei Aktionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0f406-113">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="0f406-114">Fügen Sie sie dann einer Verwaltungsrichtlinienregel hinzu, und legen Sie sie auf ein Speicherkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f406-114">Then add it to a management policy rule and set to a Storage account.</span></span>

### <span data-ttu-id="0f406-115">Beispiel 2: Erstellt ein ManagementPolicy Action Group-Objekt mit sechs Aktionen für die Snapshot- und Blobversion, fügt es dann einer Verwaltungsrichtlinienregel hinzu und legt es auf ein Speicherkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f406-115">Example 2: Creates a ManagementPolicy Action Group object with 6 actions on snapshot and blob version, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction  -SnapshotAction Delete -daysAfterCreationGreaterThan 40
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToArchive -daysAfterCreationGreaterThan 50
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToCool -daysAfterCreationGreaterThan 60
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction Delete -daysAfterCreationGreaterThan 70
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToArchive -daysAfterCreationGreaterThan 80
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToCool -daysAfterCreationGreaterThan 90
PS C:\> $action

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 60
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 50
Snapshot.Delete.DaysAfterCreationGreaterThan            : 40
Version.TierToCool.DaysAfterCreationGreaterThan         : 90
Version.TierToArchive.DaysAfterCreationGreaterThan      : 80
Version.Delete.DaysAfterCreationGreaterThan             : 70

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="0f406-116">Mit dem ersten Befehl wird ein ManagementPolicy-Aktionsgruppe-Objekt erstellt, mit den folgenden fünf Befehlen werden dem Objekt fünf Aktionen zur Snapshot- und Blobversion hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0f406-116">The first command create a ManagementPolicy Action Group object, the following 5 commands add 5 actions on snapshot and blob version to the object.</span></span> <span data-ttu-id="0f406-117">Fügen Sie sie dann einer Verwaltungsrichtlinienregel hinzu, und legen Sie sie auf ein Speicherkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f406-117">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="0f406-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0f406-118">PARAMETERS</span></span>

### <span data-ttu-id="0f406-119">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="0f406-119">-BaseBlobAction</span></span>
<span data-ttu-id="0f406-120">Die Verwaltungsrichtlinienaktion für Baseblob.</span><span class="sxs-lookup"><span data-stu-id="0f406-120">The management policy action for baseblob.</span></span>

```yaml
Type: System.String
Parameter Sets: BaseBlob
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f406-121">-BlobVersionAction</span><span class="sxs-lookup"><span data-stu-id="0f406-121">-BlobVersionAction</span></span>
<span data-ttu-id="0f406-122">Die Verwaltungsrichtlinienaktion für die Blobversion.</span><span class="sxs-lookup"><span data-stu-id="0f406-122">The management policy action for blob version.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobVersion
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f406-123">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="0f406-123">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="0f406-124">Ganzzahlwert, der das Alter in Tagen nach der Erstellung angibt.</span><span class="sxs-lookup"><span data-stu-id="0f406-124">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot, BlobVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f406-125">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="0f406-125">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="0f406-126">Ganzzahlwert, der das Alter in Tagen nach der letzten Änderung angibt.</span><span class="sxs-lookup"><span data-stu-id="0f406-126">Integer value indicating the age in days after last modification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BaseBlob
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f406-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f406-127">-DefaultProfile</span></span>
<span data-ttu-id="0f406-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f406-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f406-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f406-129">-InputObject</span></span>
<span data-ttu-id="0f406-130">Wenn Sie das ManagementPolicy-Action-Objekt eingeben, wird die Aktion auf das Eingabeaktionsobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0f406-130">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="0f406-131">Wenn sie nicht eingegeben wird, wird ein neues Aktionsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="0f406-131">If not input, will create a new action object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f406-132">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="0f406-132">-SnapshotAction</span></span>
<span data-ttu-id="0f406-133">Die Verwaltungsrichtlinienaktion für die Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="0f406-133">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f406-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f406-134">CommonParameters</span></span>
<span data-ttu-id="0f406-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f406-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f406-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f406-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f406-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f406-137">INPUTS</span></span>

### <span data-ttu-id="0f406-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="0f406-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="0f406-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f406-139">OUTPUTS</span></span>

### <span data-ttu-id="0f406-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="0f406-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="0f406-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0f406-141">NOTES</span></span>

## <span data-ttu-id="0f406-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0f406-142">RELATED LINKS</span></span>
