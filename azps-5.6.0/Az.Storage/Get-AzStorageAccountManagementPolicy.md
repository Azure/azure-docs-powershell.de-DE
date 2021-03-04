---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/get-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: f19aaf41a7f2874e0d32df3dddec3f0b8fcb6779
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944633"
---
# <span data-ttu-id="13b99-101">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="13b99-101">Get-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="13b99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13b99-102">SYNOPSIS</span></span>
<span data-ttu-id="13b99-103">Ruft die Verwaltungsrichtlinie eines Azure Storage-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="13b99-103">Gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="13b99-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13b99-104">SYNTAX</span></span>

### <span data-ttu-id="13b99-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="13b99-105">AccountName (Default)</span></span>
```
Get-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13b99-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="13b99-106">AccountResourceId</span></span>
```
Get-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13b99-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="13b99-107">AccountObject</span></span>
```
Get-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13b99-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13b99-108">DESCRIPTION</span></span>
<span data-ttu-id="13b99-109">Das **Cmdlet Get-AzStorageAccountManagementPolicy** ruft die Verwaltungsrichtlinie eines Azure Storage-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="13b99-109">The **Get-AzStorageAccountManagementPolicy** cmdlet gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="13b99-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13b99-110">EXAMPLES</span></span>

### <span data-ttu-id="13b99-111">Beispiel 1: Holen Sie sich die Verwaltungsrichtlinie eines Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="13b99-111">Example 1: Get the management policy of a Storage account.</span></span>
```
PS C:\>Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 7:04:05 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
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
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="13b99-112">Dieser Befehl ruft die Verwaltungsrichtlinie eines Speicherkontos ab.</span><span class="sxs-lookup"><span data-stu-id="13b99-112">This command gets the management policy of a Storage account.</span></span>

## <span data-ttu-id="13b99-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="13b99-113">PARAMETERS</span></span>

### <span data-ttu-id="13b99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b99-114">-DefaultProfile</span></span>
<span data-ttu-id="13b99-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13b99-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13b99-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13b99-116">-ResourceGroupName</span></span>
<span data-ttu-id="13b99-117">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="13b99-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b99-118">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="13b99-118">-StorageAccount</span></span>
<span data-ttu-id="13b99-119">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="13b99-119">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13b99-120">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="13b99-120">-StorageAccountName</span></span>
<span data-ttu-id="13b99-121">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="13b99-121">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13b99-122">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="13b99-122">-StorageAccountResourceId</span></span>
<span data-ttu-id="13b99-123">Ressourcen-ID des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="13b99-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13b99-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b99-124">CommonParameters</span></span>
<span data-ttu-id="13b99-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13b99-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b99-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13b99-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b99-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13b99-127">INPUTS</span></span>

### <span data-ttu-id="13b99-128">System.String</span><span class="sxs-lookup"><span data-stu-id="13b99-128">System.String</span></span>

## <span data-ttu-id="13b99-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13b99-129">OUTPUTS</span></span>

### <span data-ttu-id="13b99-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="13b99-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="13b99-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="13b99-131">NOTES</span></span>

## <span data-ttu-id="13b99-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="13b99-132">RELATED LINKS</span></span>
