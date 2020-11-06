---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: c63573da3c12eb54329d05f49615057d0595b77c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498162"
---
# <span data-ttu-id="aba75-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="aba75-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="aba75-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aba75-102">SYNOPSIS</span></span>
<span data-ttu-id="aba75-103">Ruft die Speicherressourcen Verwendung des aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="aba75-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aba75-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aba75-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aba75-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aba75-105">DESCRIPTION</span></span>
<span data-ttu-id="aba75-106">Das Cmdlet " **Get-AzureRmStorageUsage** " Ruft die Ressourcenverwendung für den Azure-Speicher für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="aba75-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="aba75-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aba75-107">EXAMPLES</span></span>

### <span data-ttu-id="aba75-108">Beispiel 1: Abrufen der Speicherressourcen Verwendung</span><span class="sxs-lookup"><span data-stu-id="aba75-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="aba75-109">Dieser Befehl ruft die Speicherressourcen Verwendung des aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="aba75-109">This command gets the Storage resources usage of the current subscription.</span></span>
 

### <span data-ttu-id="aba75-110">Beispiel 2: Abrufen der Speicherressourcen Verwendung des angegebenen Speicherorts</span><span class="sxs-lookup"><span data-stu-id="aba75-110">Example 2: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzureRmStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="aba75-111">Mit diesem Befehl wird die Speicherressourcen Verwendung des angegebenen Speicherorts unter dem aktuellen Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="aba75-111">This command gets the Storage resources usage of the specified location under the current subscription.</span></span>

## <span data-ttu-id="aba75-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="aba75-112">PARAMETERS</span></span>

### <span data-ttu-id="aba75-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba75-113">-DefaultProfile</span></span>
<span data-ttu-id="aba75-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aba75-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aba75-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="aba75-115">-Location</span></span>
<span data-ttu-id="aba75-116">Geben Sie an, dass die Speicherressourcen Verwendung am angegebenen Speicherort abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="aba75-116">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="aba75-117">Wenn diese nicht angegeben ist, wird die Verwendung von Speicherressourcen an allen Speicherorten unter dem Abonnement abgerufen.</span><span class="sxs-lookup"><span data-stu-id="aba75-117">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aba75-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba75-118">CommonParameters</span></span>
<span data-ttu-id="aba75-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aba75-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba75-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aba75-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba75-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aba75-121">INPUTS</span></span>

### <span data-ttu-id="aba75-122">Keine</span><span class="sxs-lookup"><span data-stu-id="aba75-122">None</span></span>

## <span data-ttu-id="aba75-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aba75-123">OUTPUTS</span></span>

### <span data-ttu-id="aba75-124">Microsoft. Azure. Commands. Management. Storage. Models. PSU</span><span class="sxs-lookup"><span data-stu-id="aba75-124">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="aba75-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="aba75-125">NOTES</span></span>

## <span data-ttu-id="aba75-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aba75-126">RELATED LINKS</span></span>

[<span data-ttu-id="aba75-127">Azure Storage Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="aba75-127">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


