---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: d6ee5a3acfd2cfafb66f0517f21f087b7a8550e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504421"
---
# <span data-ttu-id="0058d-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="0058d-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="0058d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0058d-102">SYNOPSIS</span></span>
<span data-ttu-id="0058d-103">Ruft ein Protokoll Profil ab.</span><span class="sxs-lookup"><span data-stu-id="0058d-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0058d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0058d-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0058d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0058d-105">DESCRIPTION</span></span>
<span data-ttu-id="0058d-106">Das Cmdlet " **Get-AzureRmLogProfile** " Ruft ein Protokoll Profil ab.</span><span class="sxs-lookup"><span data-stu-id="0058d-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="0058d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0058d-107">EXAMPLES</span></span>

## <span data-ttu-id="0058d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="0058d-108">PARAMETERS</span></span>

### <span data-ttu-id="0058d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0058d-109">-DefaultProfile</span></span>
<span data-ttu-id="0058d-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0058d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0058d-111">-Name</span><span class="sxs-lookup"><span data-stu-id="0058d-111">-Name</span></span>
<span data-ttu-id="0058d-112">Gibt den Namen des abzurufenden Protokoll Profils an.</span><span class="sxs-lookup"><span data-stu-id="0058d-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="0058d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0058d-113">CommonParameters</span></span>
<span data-ttu-id="0058d-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0058d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0058d-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0058d-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0058d-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0058d-116">INPUTS</span></span>

### <span data-ttu-id="0058d-117">System. String</span><span class="sxs-lookup"><span data-stu-id="0058d-117">System.String</span></span>

## <span data-ttu-id="0058d-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0058d-118">OUTPUTS</span></span>

### <span data-ttu-id="0058d-119">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="0058d-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="0058d-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="0058d-120">NOTES</span></span>

## <span data-ttu-id="0058d-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0058d-121">RELATED LINKS</span></span>

[<span data-ttu-id="0058d-122">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="0058d-122">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="0058d-123">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="0058d-123">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


