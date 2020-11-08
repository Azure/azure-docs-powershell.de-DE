---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 3d1fd5fb49b90a7d1a149cf83e8ee19c9eed5272
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173394"
---
# <span data-ttu-id="59338-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="59338-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="59338-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="59338-102">SYNOPSIS</span></span>
<span data-ttu-id="59338-103">Ruft die Speicherressourcen Verwendung des aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="59338-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="59338-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="59338-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59338-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="59338-105">DESCRIPTION</span></span>
<span data-ttu-id="59338-106">Das Cmdlet " **Get-AzStorageUsage** " Ruft die Ressourcenverwendung für den Azure-Speicher für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="59338-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="59338-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="59338-107">EXAMPLES</span></span>

### <span data-ttu-id="59338-108">Beispiel 1: Abrufen der Speicherressourcen Verwendung des angegebenen Speicherorts</span><span class="sxs-lookup"><span data-stu-id="59338-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="59338-109">Mit diesem Befehl wird die Speicherressourcen Verwendung des angegebenen Speicherorts unter dem aktuellen Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="59338-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="59338-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="59338-110">PARAMETERS</span></span>

### <span data-ttu-id="59338-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59338-111">-DefaultProfile</span></span>
<span data-ttu-id="59338-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="59338-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59338-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="59338-113">-Location</span></span>
<span data-ttu-id="59338-114">Geben Sie an, dass die Speicherressourcen Verwendung am angegebenen Speicherort abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="59338-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="59338-115">Wenn diese nicht angegeben ist, wird die Verwendung von Speicherressourcen an allen Speicherorten unter dem Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="59338-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

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

### <span data-ttu-id="59338-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59338-116">CommonParameters</span></span>
<span data-ttu-id="59338-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59338-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59338-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59338-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59338-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="59338-119">INPUTS</span></span>

### <span data-ttu-id="59338-120">System. String</span><span class="sxs-lookup"><span data-stu-id="59338-120">System.String</span></span>

## <span data-ttu-id="59338-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="59338-121">OUTPUTS</span></span>

### <span data-ttu-id="59338-122">Microsoft. Azure. Commands. Management. Storage. Models. PSU</span><span class="sxs-lookup"><span data-stu-id="59338-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="59338-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="59338-123">NOTES</span></span>

## <span data-ttu-id="59338-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="59338-124">RELATED LINKS</span></span>

[<span data-ttu-id="59338-125">Azure Storage Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="59338-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


