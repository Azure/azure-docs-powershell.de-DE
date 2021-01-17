---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 3d1fd5fb49b90a7d1a149cf83e8ee19c9eed5272
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304160"
---
# <span data-ttu-id="bf34c-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="bf34c-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="bf34c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf34c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf34c-103">Ruft die Speicherressourcennutzung des aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="bf34c-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="bf34c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf34c-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf34c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bf34c-105">DESCRIPTION</span></span>
<span data-ttu-id="bf34c-106">Das **Cmdlet "Get-AzStorageUsage"** ruft die Ressourcennutzung für Azure Storage für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="bf34c-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="bf34c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bf34c-107">EXAMPLES</span></span>

### <span data-ttu-id="bf34c-108">Beispiel 1: Erhalten der Speicherressourcennutzung des angegebenen Speicherorts</span><span class="sxs-lookup"><span data-stu-id="bf34c-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="bf34c-109">Dieser Befehl ruft die Speicherressourcennutzung des angegebenen Speicherorts unter dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="bf34c-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="bf34c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf34c-110">PARAMETERS</span></span>

### <span data-ttu-id="bf34c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf34c-111">-DefaultProfile</span></span>
<span data-ttu-id="bf34c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf34c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf34c-113">-Location</span><span class="sxs-lookup"><span data-stu-id="bf34c-113">-Location</span></span>
<span data-ttu-id="bf34c-114">Geben Sie an, dass die Speicherressourcennutzung am angegebenen Speicherort angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bf34c-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="bf34c-115">Wenn diese Angabe nicht angegeben ist, wird die Speicherressourcennutzung an allen Standorten unter dem Abonnement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bf34c-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

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

### <span data-ttu-id="bf34c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf34c-116">CommonParameters</span></span>
<span data-ttu-id="bf34c-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf34c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf34c-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf34c-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf34c-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bf34c-119">INPUTS</span></span>

### <span data-ttu-id="bf34c-120">System.String</span><span class="sxs-lookup"><span data-stu-id="bf34c-120">System.String</span></span>

## <span data-ttu-id="bf34c-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bf34c-121">OUTPUTS</span></span>

### <span data-ttu-id="bf34c-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="bf34c-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="bf34c-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bf34c-123">NOTES</span></span>

## <span data-ttu-id="bf34c-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bf34c-124">RELATED LINKS</span></span>

[<span data-ttu-id="bf34c-125">Azure Storage Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bf34c-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


