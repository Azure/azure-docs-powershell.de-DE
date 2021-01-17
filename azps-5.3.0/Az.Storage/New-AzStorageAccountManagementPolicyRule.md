---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: c2a20d19676cff15ff26792a81bfc09242c5e4c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469264"
---
# <span data-ttu-id="2c6f8-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2c6f8-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="2c6f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c6f8-102">SYNOPSIS</span></span>
<span data-ttu-id="2c6f8-103">Erstellt ein ManagementPolicy-Regelobjekt, das in Set-AzStorageAccountManagementPolicy verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="2c6f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c6f8-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c6f8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c6f8-105">DESCRIPTION</span></span>
<span data-ttu-id="2c6f8-106">Das **Cmdlet "New-AzStorageAccountManagementPolicyRule"** erstellt ein ManagementPolicy-Regelobjekt, das in Set-AzStorageAccountManagementPolicy verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="2c6f8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2c6f8-107">EXAMPLES</span></span>

### <span data-ttu-id="2c6f8-108">Beispiel 1: Erstellt ein Verwaltungspolicy-Regelobjekt, das dann auf ein Speicherkonto festgelegt wird</span><span class="sxs-lookup"><span data-stu-id="2c6f8-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2

PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name rule1 -Action $action -Filter $filter
PS C:\>$rule

Enabled    : True
Name       : rule1
Definition : {
                 "Actions":  {
                                 "BaseBlob":  {
                                                  "TierToCool":  {
                                                                     "DaysAfterModificationGreaterThan":  30
                                                                 },
                                                  "TierToArchive":  {
                                                                        "DaysAfterModificationGreaterThan":  50
                                                                    },
                                                  "Delete":  {
                                                                 "DaysAfterModificationGreaterThan":  100
                                                             }
                                              },
                                 "Snapshot":  {
                                                  "Delete":  {
                                                                 "DaysAfterCreationGreaterThan":  100
                                                             }
                                              }
                             },
                 "Filters":  {
                                 "PrefixMatch":  [
                                                     "blobprefix1",
                                                     "blobprefix2"
                                                 ],
                                 "BlobTypes":  [
                                                   "blockBlob"
                                               ]
                             }
             }

PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="2c6f8-109">Mit diesem Befehl wird ein Verwaltungspolicy-Regelobjekt erstellt, mit einem Verwaltungspolicy-Aktionsgruppesobjekt, das vier Aktionen enthält, ein Verwaltungspolicy-Regelfilterobjekt, und legen Sie die Regel dann auf ein Speicherkonto festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="2c6f8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c6f8-110">PARAMETERS</span></span>

### <span data-ttu-id="2c6f8-111">-Action</span><span class="sxs-lookup"><span data-stu-id="2c6f8-111">-Action</span></span>
<span data-ttu-id="2c6f8-112">Ein Objekt, das den Aktionssatz definiert.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-112">An object that defines the action set.</span></span>
<span data-ttu-id="2c6f8-113">Objekt mit Cmdlet-Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="2c6f8-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c6f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c6f8-114">-DefaultProfile</span></span>
<span data-ttu-id="2c6f8-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c6f8-116">-Disabled</span><span class="sxs-lookup"><span data-stu-id="2c6f8-116">-Disabled</span></span>
<span data-ttu-id="2c6f8-117">Die Regel ist deaktiviert, wenn sie festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-117">The rule is disabled if set it.</span></span>

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

### <span data-ttu-id="2c6f8-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="2c6f8-118">-Filter</span></span>
<span data-ttu-id="2c6f8-119">Ein Objekt, das den Filtersatz definiert.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-119">An object that defines the filter set.</span></span>
<span data-ttu-id="2c6f8-120">Objekt mit Cmdlet-New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="2c6f8-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c6f8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2c6f8-121">-Name</span></span>
<span data-ttu-id="2c6f8-122">Ein Regelname kann eine beliebige Kombination alphanumerischer Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="2c6f8-123">Bei Regelnamen muss die Zwischen- und Kleinschreibung beachtet werden.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="2c6f8-124">Sie muss innerhalb einer Richtlinie eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-124">It must be unique within a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c6f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c6f8-125">CommonParameters</span></span>
<span data-ttu-id="2c6f8-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c6f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c6f8-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c6f8-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c6f8-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2c6f8-128">INPUTS</span></span>

### <span data-ttu-id="2c6f8-129">Keine</span><span class="sxs-lookup"><span data-stu-id="2c6f8-129">None</span></span>

## <span data-ttu-id="2c6f8-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2c6f8-130">OUTPUTS</span></span>

### <span data-ttu-id="2c6f8-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2c6f8-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="2c6f8-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2c6f8-132">NOTES</span></span>

## <span data-ttu-id="2c6f8-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2c6f8-133">RELATED LINKS</span></span>
