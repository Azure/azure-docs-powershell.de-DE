---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
ms.openlocfilehash: 64cf2a14791796e2796f15e446e6ceb29b5b24cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663163"
---
# <span data-ttu-id="1aa5f-101">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="1aa5f-101">Get-AzureRmDataLakeStoreChildItem</span></span>

## <span data-ttu-id="1aa5f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1aa5f-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa5f-103">Ruft die Liste der Elemente in einem Ordner im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="1aa5f-103">Gets the list of items in a folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1aa5f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1aa5f-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aa5f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1aa5f-105">DESCRIPTION</span></span>
<span data-ttu-id="1aa5f-106">Das Cmdlet " **Get-AzureRmDataLakeStoreChildItem** " Ruft die Liste der Elemente in einem Ordner im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="1aa5f-106">The **Get-AzureRmDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="1aa5f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1aa5f-107">EXAMPLES</span></span>

### <span data-ttu-id="1aa5f-108">Beispiel 1: Abrufen der untergeordneten Elemente für einen Ordner</span><span class="sxs-lookup"><span data-stu-id="1aa5f-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="1aa5f-109">Dieser Befehl ruft die untergeordneten Elemente für den Ordner "meine Dateien" ab.</span><span class="sxs-lookup"><span data-stu-id="1aa5f-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="1aa5f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1aa5f-110">PARAMETERS</span></span>

### <span data-ttu-id="1aa5f-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="1aa5f-111">-Account</span></span>
<span data-ttu-id="1aa5f-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="1aa5f-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1aa5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa5f-113">-DefaultProfile</span></span>
<span data-ttu-id="1aa5f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1aa5f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1aa5f-115">-Path</span><span class="sxs-lookup"><span data-stu-id="1aa5f-115">-Path</span></span>
<span data-ttu-id="1aa5f-116">Gibt den Daten See-Speicherpfad des Ordners an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="1aa5f-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1aa5f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa5f-117">CommonParameters</span></span>
<span data-ttu-id="1aa5f-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aa5f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa5f-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aa5f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa5f-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1aa5f-120">INPUTS</span></span>

### <span data-ttu-id="1aa5f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1aa5f-121">System.String</span></span>

### <span data-ttu-id="1aa5f-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1aa5f-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="1aa5f-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1aa5f-123">OUTPUTS</span></span>

### <span data-ttu-id="1aa5f-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1aa5f-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="1aa5f-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="1aa5f-125">NOTES</span></span>

## <span data-ttu-id="1aa5f-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1aa5f-126">RELATED LINKS</span></span>
