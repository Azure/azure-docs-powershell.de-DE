---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: 51dd39f18874fc1888fb37277f5de0557cf3553b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932619"
---
# <span data-ttu-id="8e3f2-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="8e3f2-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="8e3f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e3f2-102">SYNOPSIS</span></span>
<span data-ttu-id="8e3f2-103">Ruft ein Protokollprofil ab.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-103">Gets a log profile.</span></span>

## <span data-ttu-id="8e3f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e3f2-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e3f2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e3f2-105">DESCRIPTION</span></span>
<span data-ttu-id="8e3f2-106">Das **Get-AzLogProfile-Cmdlet** erhält ein Protokollprofil.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="8e3f2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e3f2-107">EXAMPLES</span></span>

## <span data-ttu-id="8e3f2-108">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8e3f2-108">PARAMETERS</span></span>

### <span data-ttu-id="8e3f2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e3f2-109">-DefaultProfile</span></span>
<span data-ttu-id="8e3f2-110">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8e3f2-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e3f2-111">-Name</span><span class="sxs-lookup"><span data-stu-id="8e3f2-111">-Name</span></span>
<span data-ttu-id="8e3f2-112">Gibt den Namen des zu erhaltenden Protokollprofils an.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="8e3f2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e3f2-113">CommonParameters</span></span>
<span data-ttu-id="8e3f2-114">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e3f2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e3f2-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e3f2-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e3f2-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e3f2-116">INPUTS</span></span>

### <span data-ttu-id="8e3f2-117">System.String</span><span class="sxs-lookup"><span data-stu-id="8e3f2-117">System.String</span></span>

## <span data-ttu-id="8e3f2-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e3f2-118">OUTPUTS</span></span>

### <span data-ttu-id="8e3f2-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="8e3f2-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="8e3f2-120">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8e3f2-120">NOTES</span></span>

## <span data-ttu-id="8e3f2-121">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8e3f2-121">RELATED LINKS</span></span>

[<span data-ttu-id="8e3f2-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="8e3f2-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="8e3f2-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="8e3f2-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


