---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
ms.openlocfilehash: ae6524c46ed97563e7bf6c948f550a393d74f582
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848984"
---
# <span data-ttu-id="dad49-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="dad49-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="dad49-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dad49-102">SYNOPSIS</span></span>
<span data-ttu-id="dad49-103">Ruft die Speicherressourcen Verwendung des aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="dad49-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dad49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dad49-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dad49-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dad49-105">DESCRIPTION</span></span>
<span data-ttu-id="dad49-106">Das Cmdlet " **Get-AzureRmStorageUsage** " Ruft die Ressourcenverwendung für den Azure-Speicher für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="dad49-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="dad49-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dad49-107">EXAMPLES</span></span>

### <span data-ttu-id="dad49-108">Beispiel 1: Abrufen der Speicherressourcen Verwendung</span><span class="sxs-lookup"><span data-stu-id="dad49-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="dad49-109">Dieser Befehl ruft die Speicherressourcen Verwendung des aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="dad49-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="dad49-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dad49-110">PARAMETERS</span></span>

### <span data-ttu-id="dad49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad49-111">-DefaultProfile</span></span>
<span data-ttu-id="dad49-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dad49-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dad49-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad49-113">CommonParameters</span></span>
<span data-ttu-id="dad49-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad49-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad49-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad49-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad49-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dad49-116">INPUTS</span></span>

### <span data-ttu-id="dad49-117">Keine</span><span class="sxs-lookup"><span data-stu-id="dad49-117">None</span></span>

## <span data-ttu-id="dad49-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dad49-118">OUTPUTS</span></span>

### <span data-ttu-id="dad49-119">Microsoft. Azure. Commands. Management. Storage. Models. PSU</span><span class="sxs-lookup"><span data-stu-id="dad49-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="dad49-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="dad49-120">NOTES</span></span>

## <span data-ttu-id="dad49-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dad49-121">RELATED LINKS</span></span>

[<span data-ttu-id="dad49-122">Azure Storage Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="dad49-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


