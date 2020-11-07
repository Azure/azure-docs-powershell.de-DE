---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: 195ef931b942f3dc8a88ede7e3feb31a3b8aa77f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826684"
---
# <span data-ttu-id="5668b-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="5668b-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="5668b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5668b-102">SYNOPSIS</span></span>
<span data-ttu-id="5668b-103">Erstellt ein ManagementPolicy-Regelobjekt, das in Satz-AzStorageAccountManagementPolicy verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5668b-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="5668b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5668b-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5668b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5668b-105">DESCRIPTION</span></span>
<span data-ttu-id="5668b-106">Mit dem Cmdlet **New-AzStorageAccountManagementPolicyRule** wird ein ManagementPolicy-Regelobjekt erstellt, das in der Gruppe AzStorageAccountManagementPolicy verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5668b-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="5668b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5668b-107">EXAMPLES</span></span>

### <span data-ttu-id="5668b-108">Beispiel 1: erstellt ein ManagementPolicy-Regelobjekt und wird dann auf ein Speicherkonto gesetzt.</span><span class="sxs-lookup"><span data-stu-id="5668b-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
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

<span data-ttu-id="5668b-109">Mit diesem Befehl wird ein ManagementPolicy-Regelobjekt erstellt, wobei ein ManagementPolicy-Aktionsgruppen Objekt 4 Aktionen enthält, ein ManagementPolicy-Regelfilter Objekt, und dann die Regel auf ein Speicherkonto legen.</span><span class="sxs-lookup"><span data-stu-id="5668b-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="5668b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5668b-110">PARAMETERS</span></span>

### <span data-ttu-id="5668b-111">– Aktion</span><span class="sxs-lookup"><span data-stu-id="5668b-111">-Action</span></span>
<span data-ttu-id="5668b-112">Ein Objekt, das den Aktionssatz definiert.</span><span class="sxs-lookup"><span data-stu-id="5668b-112">An object that defines the action set.</span></span>
<span data-ttu-id="5668b-113">Abrufen des Objekts mit dem Cmdlet Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="5668b-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

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

### <span data-ttu-id="5668b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5668b-114">-DefaultProfile</span></span>
<span data-ttu-id="5668b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5668b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5668b-116">-Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="5668b-116">-Disabled</span></span>
<span data-ttu-id="5668b-117">Die Regel ist deaktiviert, wenn Sie Sie einrichten.</span><span class="sxs-lookup"><span data-stu-id="5668b-117">The rule is disabled if set it.</span></span>

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

### <span data-ttu-id="5668b-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="5668b-118">-Filter</span></span>
<span data-ttu-id="5668b-119">Ein Objekt, das den Filtersatz definiert.</span><span class="sxs-lookup"><span data-stu-id="5668b-119">An object that defines the filter set.</span></span>
<span data-ttu-id="5668b-120">Abrufen des Objekts mit dem Cmdlet New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="5668b-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

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

### <span data-ttu-id="5668b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5668b-121">-Name</span></span>
<span data-ttu-id="5668b-122">Ein Regelname kann eine beliebige Kombination aus alphanumerischen Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5668b-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="5668b-123">Beim Regelnamen wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="5668b-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="5668b-124">Sie muss innerhalb einer Richtlinie eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="5668b-124">It must be unique within a policy.</span></span>

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

### <span data-ttu-id="5668b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5668b-125">CommonParameters</span></span>
<span data-ttu-id="5668b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5668b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5668b-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5668b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5668b-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5668b-128">INPUTS</span></span>

### <span data-ttu-id="5668b-129">Keine</span><span class="sxs-lookup"><span data-stu-id="5668b-129">None</span></span>

## <span data-ttu-id="5668b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5668b-130">OUTPUTS</span></span>

### <span data-ttu-id="5668b-131">Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="5668b-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="5668b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="5668b-132">NOTES</span></span>

## <span data-ttu-id="5668b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5668b-133">RELATED LINKS</span></span>
