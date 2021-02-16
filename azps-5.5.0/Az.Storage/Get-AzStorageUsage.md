---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 3d1fd5fb49b90a7d1a149cf83e8ee19c9eed5272
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150428"
---
# <span data-ttu-id="5d96b-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="5d96b-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="5d96b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d96b-102">SYNOPSIS</span></span>
<span data-ttu-id="5d96b-103">Ruft die Speicherressourcennutzung des aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="5d96b-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="5d96b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d96b-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d96b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d96b-105">DESCRIPTION</span></span>
<span data-ttu-id="5d96b-106">Das **Cmdlet "Get-AzStorageUsage"** ruft die Ressourcennutzung für Azure Storage für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5d96b-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="5d96b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5d96b-107">EXAMPLES</span></span>

### <span data-ttu-id="5d96b-108">Beispiel 1: Erhalten der Speicherressourcennutzung des angegebenen Speicherorts</span><span class="sxs-lookup"><span data-stu-id="5d96b-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="5d96b-109">Dieser Befehl ruft die Speicherressourcennutzung des angegebenen Speicherorts unter dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5d96b-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="5d96b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d96b-110">PARAMETERS</span></span>

### <span data-ttu-id="5d96b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d96b-111">-DefaultProfile</span></span>
<span data-ttu-id="5d96b-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5d96b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d96b-113">-Location</span><span class="sxs-lookup"><span data-stu-id="5d96b-113">-Location</span></span>
<span data-ttu-id="5d96b-114">Geben Sie an, dass die Speicherressourcennutzung am angegebenen Speicherort angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5d96b-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="5d96b-115">Wenn diese Angabe nicht angegeben ist, wird die Speicherressourcennutzung an allen Standorten unter dem Abonnement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5d96b-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d96b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d96b-116">CommonParameters</span></span>
<span data-ttu-id="5d96b-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d96b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d96b-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d96b-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d96b-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5d96b-119">INPUTS</span></span>

### <span data-ttu-id="5d96b-120">System.String</span><span class="sxs-lookup"><span data-stu-id="5d96b-120">System.String</span></span>

## <span data-ttu-id="5d96b-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5d96b-121">OUTPUTS</span></span>

### <span data-ttu-id="5d96b-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="5d96b-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="5d96b-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5d96b-123">NOTES</span></span>

## <span data-ttu-id="5d96b-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5d96b-124">RELATED LINKS</span></span>

[<span data-ttu-id="5d96b-125">Azure Storage Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5d96b-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


