---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzLogProfile.md
ms.openlocfilehash: fa8c7768f2fcea53157f1b7bb3d89a5567ecdf2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359230"
---
# <span data-ttu-id="45977-101">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="45977-101">Get-AzLogProfile</span></span>

## <span data-ttu-id="45977-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45977-102">SYNOPSIS</span></span>
<span data-ttu-id="45977-103">Ruft ein Protokollprofil ab.</span><span class="sxs-lookup"><span data-stu-id="45977-103">Gets a log profile.</span></span>

## <span data-ttu-id="45977-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45977-104">SYNTAX</span></span>

```
Get-AzLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45977-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45977-105">DESCRIPTION</span></span>
<span data-ttu-id="45977-106">Das **Cmdlet "Get-AzLogProfile"** ruft ein Protokollprofil ab.</span><span class="sxs-lookup"><span data-stu-id="45977-106">The **Get-AzLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="45977-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="45977-107">EXAMPLES</span></span>

## <span data-ttu-id="45977-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45977-108">PARAMETERS</span></span>

### <span data-ttu-id="45977-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45977-109">-DefaultProfile</span></span>
<span data-ttu-id="45977-110">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="45977-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45977-111">-Name</span><span class="sxs-lookup"><span data-stu-id="45977-111">-Name</span></span>
<span data-ttu-id="45977-112">Gibt den Namen des zu erhaltenden Protokollprofils an.</span><span class="sxs-lookup"><span data-stu-id="45977-112">Specifies the name of the log profile to get.</span></span>

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

### <span data-ttu-id="45977-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45977-113">CommonParameters</span></span>
<span data-ttu-id="45977-114">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45977-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45977-115">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45977-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45977-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="45977-116">INPUTS</span></span>

### <span data-ttu-id="45977-117">System.String</span><span class="sxs-lookup"><span data-stu-id="45977-117">System.String</span></span>

## <span data-ttu-id="45977-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="45977-118">OUTPUTS</span></span>

### <span data-ttu-id="45977-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="45977-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="45977-120">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="45977-120">NOTES</span></span>

## <span data-ttu-id="45977-121">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="45977-121">RELATED LINKS</span></span>

[<span data-ttu-id="45977-122">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="45977-122">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="45977-123">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="45977-123">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)


