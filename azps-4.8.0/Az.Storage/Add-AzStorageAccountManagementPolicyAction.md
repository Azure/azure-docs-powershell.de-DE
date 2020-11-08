---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: ed876765e3b5eb9d306847958772d9205758f5d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010417"
---
# <span data-ttu-id="5f5e8-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="5f5e8-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="5f5e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="5f5e8-103">Fügt dem Eingabe ManagementPolicy-Aktionsgruppen Objekt eine Aktion hinzu oder erstellt ein ManagementPolicy-Aktionsgruppen Objekt mit der Aktion.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="5f5e8-104">Das Objekt kann in New-AzStorageAccountManagementPolicyRule verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="5f5e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f5e8-105">SYNTAX</span></span>

### <span data-ttu-id="5f5e8-106">BaseBlob (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f5e8-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f5e8-107">Snapshot</span><span class="sxs-lookup"><span data-stu-id="5f5e8-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f5e8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f5e8-108">DESCRIPTION</span></span>
<span data-ttu-id="5f5e8-109">Das **Add-AzStorageAccountManagementPolicyAction-** Cmdlet fügt dem Eingabe ManagementPolicy-Aktionsgruppen Objekt eine Aktion hinzu oder erstellt ein ManagementPolicy-Aktionsgruppen Objekt mit der Aktion.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="5f5e8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f5e8-110">EXAMPLES</span></span>

### <span data-ttu-id="5f5e8-111">Beispiel 1: erstellt ein ManagementPolicy-Aktionsgruppen Objekt mit 4 Aktionen, fügt es dann einer Verwaltungsrichtlinien Regel hinzu und legt es auf ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
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

<span data-ttu-id="5f5e8-112">Mit dem ersten Befehl wird ein ManagementPolicy-Aktionsgruppen Objekt erstellt, mit den folgenden 3 Befehlen werden dem Objekt 3 Aktionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="5f5e8-113">Fügen Sie es dann einer Verwaltungsrichtlinien Regel hinzu, und legen Sie es auf ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="5f5e8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f5e8-114">PARAMETERS</span></span>

### <span data-ttu-id="5f5e8-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="5f5e8-115">-BaseBlobAction</span></span>
<span data-ttu-id="5f5e8-116">Die Verwaltungsrichtlinien Aktion für baseblob.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-116">The management policy action for baseblob.</span></span>

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

### <span data-ttu-id="5f5e8-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="5f5e8-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="5f5e8-118">Ganzzahliger Wert, der das Alter in Tagen nach der Erstellung angibt.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-118">Integer value indicating the age in days after creation.</span></span>

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

### <span data-ttu-id="5f5e8-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="5f5e8-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="5f5e8-120">Ganzzahliger Wert, der das Alter in Tagen nach der letzten Änderung angibt.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-120">Integer value indicating the age in days after last modification.</span></span>

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

### <span data-ttu-id="5f5e8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f5e8-121">-DefaultProfile</span></span>
<span data-ttu-id="5f5e8-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f5e8-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5f5e8-123">-InputObject</span></span>
<span data-ttu-id="5f5e8-124">Wenn das ManagementPolicy-Aktionsobjekt eingegeben wird, wird die Aktion auf das Eingabe Aktionsobjekt gesetzt.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="5f5e8-125">Wenn nicht eingegeben, wird ein neues Aktionsobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-125">If not input, will create a new action object.</span></span>

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

### <span data-ttu-id="5f5e8-126">-Schnappschuss</span><span class="sxs-lookup"><span data-stu-id="5f5e8-126">-SnapshotAction</span></span>
<span data-ttu-id="5f5e8-127">Die Verwaltungsrichtlinien Aktion für Snapshot.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-127">The management policy action for snapshot.</span></span>

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

### <span data-ttu-id="5f5e8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f5e8-128">CommonParameters</span></span>
<span data-ttu-id="5f5e8-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f5e8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f5e8-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f5e8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f5e8-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f5e8-131">INPUTS</span></span>

### <span data-ttu-id="5f5e8-132">Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="5f5e8-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="5f5e8-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f5e8-133">OUTPUTS</span></span>

### <span data-ttu-id="5f5e8-134">Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="5f5e8-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="5f5e8-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f5e8-135">NOTES</span></span>

## <span data-ttu-id="5f5e8-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f5e8-136">RELATED LINKS</span></span>
