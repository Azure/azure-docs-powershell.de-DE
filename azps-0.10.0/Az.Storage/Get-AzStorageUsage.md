---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: edf78ad4022b29251d78e976ff7e5d66ae67bb69
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843032"
---
# <span data-ttu-id="93486-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="93486-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="93486-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93486-102">SYNOPSIS</span></span>
<span data-ttu-id="93486-103">Ruft die Speicherressourcen Verwendung des aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="93486-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="93486-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93486-104">SYNTAX</span></span>

```
Get-AzStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93486-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93486-105">DESCRIPTION</span></span>
<span data-ttu-id="93486-106">Das Cmdlet " **Get-AzStorageUsage** " Ruft die Ressourcenverwendung für den Azure-Speicher für das aktuelle Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="93486-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="93486-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93486-107">EXAMPLES</span></span>

### <span data-ttu-id="93486-108">Beispiel 1: Abrufen der Speicherressourcen Verwendung</span><span class="sxs-lookup"><span data-stu-id="93486-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzStorageUsage
```

<span data-ttu-id="93486-109">Dieser Befehl ruft die Speicherressourcen Verwendung des aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="93486-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="93486-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="93486-110">PARAMETERS</span></span>

### <span data-ttu-id="93486-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93486-111">-DefaultProfile</span></span>
<span data-ttu-id="93486-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93486-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93486-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93486-113">CommonParameters</span></span>
<span data-ttu-id="93486-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93486-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93486-115">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93486-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93486-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93486-116">INPUTS</span></span>

### <span data-ttu-id="93486-117">Keine</span><span class="sxs-lookup"><span data-stu-id="93486-117">None</span></span>

## <span data-ttu-id="93486-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93486-118">OUTPUTS</span></span>

### <span data-ttu-id="93486-119">Microsoft. Azure. Commands. Management. Storage. Models. PSU</span><span class="sxs-lookup"><span data-stu-id="93486-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="93486-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="93486-120">NOTES</span></span>

## <span data-ttu-id="93486-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93486-121">RELATED LINKS</span></span>

[<span data-ttu-id="93486-122">Azure Storage Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="93486-122">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


