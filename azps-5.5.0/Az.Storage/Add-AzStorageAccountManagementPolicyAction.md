---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: ed876765e3b5eb9d306847958772d9205758f5d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143892"
---
# <span data-ttu-id="504b0-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="504b0-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="504b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="504b0-102">SYNOPSIS</span></span>
<span data-ttu-id="504b0-103">Fügt dem Objekt "Input ManagementPolicy Action Group" eine Aktion hinzu oder erstellt ein Objekt der Aktionsgruppe "ManagementPolicy" mit der Aktion.</span><span class="sxs-lookup"><span data-stu-id="504b0-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="504b0-104">Das Objekt kann in "New-AzStorageAccountManagementPolicyRule" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="504b0-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="504b0-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="504b0-105">SYNTAX</span></span>

### <span data-ttu-id="504b0-106">BaseBlob (Standard)</span><span class="sxs-lookup"><span data-stu-id="504b0-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="504b0-107">Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="504b0-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="504b0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="504b0-108">DESCRIPTION</span></span>
<span data-ttu-id="504b0-109">Das **Cmdlet "Add-AzStorageAccountManagementPolicyAction"** fügt dem Eingabeobjekt "ManagementPolicy Action Group" eine Aktion hinzu oder erstellt mit der Aktion ein Verwaltungspolicy-Aktionsgruppe-Objekt.</span><span class="sxs-lookup"><span data-stu-id="504b0-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="504b0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="504b0-110">EXAMPLES</span></span>

### <span data-ttu-id="504b0-111">Beispiel 1: Erstellt ein Objekt der Aktionsgruppe "ManagementPolicy" mit vier Aktionen. Anschließend fügen Sie es einer Verwaltungsrichtlinienregel hinzu und legen es auf ein Speicherkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="504b0-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="504b0-112">Mit dem ersten Befehl wird ein Objekt der Aktionsgruppe "ManagementPolicy" erstellt, mit den folgenden drei Befehlen werden dem Objekt drei Aktionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="504b0-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="504b0-113">Fügen Sie sie dann einer Verwaltungsrichtlinienregel hinzu, und legen Sie sie auf ein Speicherkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="504b0-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="504b0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="504b0-114">PARAMETERS</span></span>

### <span data-ttu-id="504b0-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="504b0-115">-BaseBlobAction</span></span>
<span data-ttu-id="504b0-116">Die Verwaltungsrichtlinienaktion für Baseblob.</span><span class="sxs-lookup"><span data-stu-id="504b0-116">The management policy action for baseblob.</span></span>

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

### <span data-ttu-id="504b0-117">-DaysAfterCreationGreater1</span><span class="sxs-lookup"><span data-stu-id="504b0-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="504b0-118">Ganzzahliger Wert, der das Alter in Tagen nach Erstellung angibt.</span><span class="sxs-lookup"><span data-stu-id="504b0-118">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504b0-119">-DaysAfterModificationGreater 1</span><span class="sxs-lookup"><span data-stu-id="504b0-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="504b0-120">Ganzzahliger Wert, der das Alter in Tagen nach der letzten Änderung angibt.</span><span class="sxs-lookup"><span data-stu-id="504b0-120">Integer value indicating the age in days after last modification.</span></span>

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

### <span data-ttu-id="504b0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="504b0-121">-DefaultProfile</span></span>
<span data-ttu-id="504b0-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="504b0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="504b0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="504b0-123">-InputObject</span></span>
<span data-ttu-id="504b0-124">Wenn Sie das Verwaltungspolicy-Aktionsobjekt eingeben, wird die Aktion auf das Eingabeaktionsobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="504b0-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="504b0-125">Wenn keine Eingabe verwendet wird, wird ein neues Aktionsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="504b0-125">If not input, will create a new action object.</span></span>

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

### <span data-ttu-id="504b0-126">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="504b0-126">-SnapshotAction</span></span>
<span data-ttu-id="504b0-127">Die Verwaltungsrichtlinienaktion für Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="504b0-127">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504b0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="504b0-128">CommonParameters</span></span>
<span data-ttu-id="504b0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="504b0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="504b0-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="504b0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="504b0-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="504b0-131">INPUTS</span></span>

### <span data-ttu-id="504b0-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="504b0-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="504b0-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="504b0-133">OUTPUTS</span></span>

### <span data-ttu-id="504b0-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="504b0-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="504b0-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="504b0-135">NOTES</span></span>

## <span data-ttu-id="504b0-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="504b0-136">RELATED LINKS</span></span>
