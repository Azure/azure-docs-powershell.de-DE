---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: e27fde6a25fc512b898ded7d4f087ab7b344d293
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921264"
---
# <span data-ttu-id="1589b-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="1589b-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="1589b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1589b-102">SYNOPSIS</span></span>
<span data-ttu-id="1589b-103">Ruft die Liste der Elemente in einem Ordner im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="1589b-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="1589b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1589b-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1589b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1589b-105">DESCRIPTION</span></span>
<span data-ttu-id="1589b-106">Das **Get-AzDataLakeStoreChildItem-Cmdlet** ruft die Liste der Elemente in einem Ordner im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="1589b-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="1589b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1589b-107">EXAMPLES</span></span>

### <span data-ttu-id="1589b-108">Beispiel 1: Erhalten der untergeordneten Elemente für einen Ordner</span><span class="sxs-lookup"><span data-stu-id="1589b-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="1589b-109">Dieser Befehl ruft die untergeordneten Elemente für den Ordner "MyFiles" ab.</span><span class="sxs-lookup"><span data-stu-id="1589b-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="1589b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1589b-110">PARAMETERS</span></span>

### <span data-ttu-id="1589b-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="1589b-111">-Account</span></span>
<span data-ttu-id="1589b-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="1589b-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1589b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1589b-113">-DefaultProfile</span></span>
<span data-ttu-id="1589b-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1589b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1589b-115">-Path</span><span class="sxs-lookup"><span data-stu-id="1589b-115">-Path</span></span>
<span data-ttu-id="1589b-116">Gibt den Data Lake Store-Pfad des Ordners an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="1589b-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1589b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1589b-117">CommonParameters</span></span>
<span data-ttu-id="1589b-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1589b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1589b-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1589b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1589b-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1589b-120">INPUTS</span></span>

### <span data-ttu-id="1589b-121">System.String</span><span class="sxs-lookup"><span data-stu-id="1589b-121">System.String</span></span>

### <span data-ttu-id="1589b-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1589b-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="1589b-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1589b-123">OUTPUTS</span></span>

### <span data-ttu-id="1589b-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1589b-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="1589b-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1589b-125">NOTES</span></span>

## <span data-ttu-id="1589b-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1589b-126">RELATED LINKS</span></span>
