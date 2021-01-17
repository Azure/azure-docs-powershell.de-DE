---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: b27d6e8bec4dda2ba87a0b38a9b37a8d4739ae00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458223"
---
# <span data-ttu-id="05274-101">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="05274-101">Get-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="05274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05274-102">SYNOPSIS</span></span>
<span data-ttu-id="05274-103">Ruft die Verwaltungsrichtlinie eines Azure Storage-Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="05274-103">Gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="05274-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05274-104">SYNTAX</span></span>

### <span data-ttu-id="05274-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="05274-105">AccountName (Default)</span></span>
```
Get-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05274-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="05274-106">AccountResourceId</span></span>
```
Get-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05274-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="05274-107">AccountObject</span></span>
```
Get-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05274-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05274-108">DESCRIPTION</span></span>
<span data-ttu-id="05274-109">Das **Cmdlet "Get-AzStorageAccountManagementPolicy"** ruft die Verwaltungsrichtlinie eines Azure -Speicherkontos ab.</span><span class="sxs-lookup"><span data-stu-id="05274-109">The **Get-AzStorageAccountManagementPolicy** cmdlet gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="05274-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="05274-110">EXAMPLES</span></span>

### <span data-ttu-id="05274-111">Beispiel 1: Erhalten der Verwaltungsrichtlinie eines Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="05274-111">Example 1: Get the management policy of a Storage account.</span></span>
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

<span data-ttu-id="05274-112">Dieser Befehl ruft die Verwaltungsrichtlinie eines Speicherkontos ab.</span><span class="sxs-lookup"><span data-stu-id="05274-112">This command gets the management policy of a Storage account.</span></span>

## <span data-ttu-id="05274-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05274-113">PARAMETERS</span></span>

### <span data-ttu-id="05274-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05274-114">-DefaultProfile</span></span>
<span data-ttu-id="05274-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05274-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05274-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05274-116">-ResourceGroupName</span></span>
<span data-ttu-id="05274-117">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="05274-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="05274-118">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="05274-118">-StorageAccount</span></span>
<span data-ttu-id="05274-119">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="05274-119">Storage account object</span></span>

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

### <span data-ttu-id="05274-120">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="05274-120">-StorageAccountName</span></span>
<span data-ttu-id="05274-121">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="05274-121">Storage Account Name.</span></span>

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

### <span data-ttu-id="05274-122">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="05274-122">-StorageAccountResourceId</span></span>
<span data-ttu-id="05274-123">Ressourcen-ID des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="05274-123">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="05274-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05274-124">CommonParameters</span></span>
<span data-ttu-id="05274-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05274-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05274-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05274-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05274-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="05274-127">INPUTS</span></span>

### <span data-ttu-id="05274-128">System.String</span><span class="sxs-lookup"><span data-stu-id="05274-128">System.String</span></span>

## <span data-ttu-id="05274-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="05274-129">OUTPUTS</span></span>

### <span data-ttu-id="05274-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="05274-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="05274-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="05274-131">NOTES</span></span>

## <span data-ttu-id="05274-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="05274-132">RELATED LINKS</span></span>
