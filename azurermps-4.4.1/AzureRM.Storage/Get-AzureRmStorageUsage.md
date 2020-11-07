---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: 1ef273329634e080c4117b9ddd0d1eaf8d91bb0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665229"
---
# <span data-ttu-id="db336-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="db336-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="db336-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="db336-102">SYNOPSIS</span></span>
<span data-ttu-id="db336-103">Ruft die Speicherressourcen Verwendung des aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="db336-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db336-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="db336-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db336-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db336-105">DESCRIPTION</span></span>
<span data-ttu-id="db336-106">Das Cmdlet " **Get-AzureRmStorageUsage** " Ruft die Ressourcenverwendung für den Azure-Speicher für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="db336-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="db336-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="db336-107">EXAMPLES</span></span>

### <span data-ttu-id="db336-108">Beispiel 1: Abrufen der Speicherressourcen Verwendung</span><span class="sxs-lookup"><span data-stu-id="db336-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="db336-109">Dieser Befehl ruft die Speicherressourcen Verwendung des aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="db336-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="db336-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="db336-110">PARAMETERS</span></span>

### <span data-ttu-id="db336-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db336-111">-DefaultProfile</span></span>
<span data-ttu-id="db336-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="db336-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db336-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db336-113">CommonParameters</span></span>
<span data-ttu-id="db336-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db336-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db336-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db336-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db336-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="db336-116">INPUTS</span></span>

## <span data-ttu-id="db336-117">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="db336-117">OUTPUTS</span></span>

## <span data-ttu-id="db336-118">Notizen</span><span class="sxs-lookup"><span data-stu-id="db336-118">NOTES</span></span>

## <span data-ttu-id="db336-119">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="db336-119">RELATED LINKS</span></span>

[<span data-ttu-id="db336-120">Azure Storage Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="db336-120">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


