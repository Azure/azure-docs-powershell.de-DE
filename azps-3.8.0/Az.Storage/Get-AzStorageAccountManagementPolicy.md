---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: b27d6e8bec4dda2ba87a0b38a9b37a8d4739ae00
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997000"
---
# <span data-ttu-id="c11df-101">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c11df-101">Get-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="c11df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c11df-102">SYNOPSIS</span></span>
<span data-ttu-id="c11df-103">Ruft die Verwaltungsrichtlinie für ein Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="c11df-103">Gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="c11df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c11df-104">SYNTAX</span></span>

### <span data-ttu-id="c11df-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="c11df-105">AccountName (Default)</span></span>
```
Get-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c11df-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c11df-106">AccountResourceId</span></span>
```
Get-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c11df-107">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="c11df-107">AccountObject</span></span>
```
Get-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c11df-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c11df-108">DESCRIPTION</span></span>
<span data-ttu-id="c11df-109">Das Cmdlet " **Get-AzStorageAccountManagementPolicy** " Ruft die Verwaltungsrichtlinie für ein Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="c11df-109">The **Get-AzStorageAccountManagementPolicy** cmdlet gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="c11df-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c11df-110">EXAMPLES</span></span>

### <span data-ttu-id="c11df-111">Beispiel 1: Abrufen der Verwaltungsrichtlinie eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="c11df-111">Example 1: Get the management policy of a Storage account.</span></span>
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

<span data-ttu-id="c11df-112">Mit diesem Befehl wird die Verwaltungsrichtlinie eines speicherkontos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c11df-112">This command gets the management policy of a Storage account.</span></span>

## <span data-ttu-id="c11df-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c11df-113">PARAMETERS</span></span>

### <span data-ttu-id="c11df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c11df-114">-DefaultProfile</span></span>
<span data-ttu-id="c11df-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c11df-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c11df-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c11df-116">-ResourceGroupName</span></span>
<span data-ttu-id="c11df-117">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c11df-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="c11df-118">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c11df-118">-StorageAccount</span></span>
<span data-ttu-id="c11df-119">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="c11df-119">Storage account object</span></span>

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

### <span data-ttu-id="c11df-120">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c11df-120">-StorageAccountName</span></span>
<span data-ttu-id="c11df-121">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="c11df-121">Storage Account Name.</span></span>

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

### <span data-ttu-id="c11df-122">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c11df-122">-StorageAccountResourceId</span></span>
<span data-ttu-id="c11df-123">Ressourcen-ID des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="c11df-123">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="c11df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c11df-124">CommonParameters</span></span>
<span data-ttu-id="c11df-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c11df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c11df-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c11df-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c11df-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c11df-127">INPUTS</span></span>

### <span data-ttu-id="c11df-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c11df-128">System.String</span></span>

## <span data-ttu-id="c11df-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c11df-129">OUTPUTS</span></span>

### <span data-ttu-id="c11df-130">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c11df-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="c11df-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c11df-131">NOTES</span></span>

## <span data-ttu-id="c11df-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c11df-132">RELATED LINKS</span></span>
