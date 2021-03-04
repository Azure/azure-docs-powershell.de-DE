---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: ad005dbf386bc8340fa0da0c5e8dac1d11bf4bbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928131"
---
# <span data-ttu-id="92bb2-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="92bb2-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="92bb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="92bb2-103">Erstellen Sie ein PSHeaderAction-Objekt.</span><span class="sxs-lookup"><span data-stu-id="92bb2-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="92bb2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92bb2-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92bb2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92bb2-105">DESCRIPTION</span></span>
<span data-ttu-id="92bb2-106">Erstellt ein PSHeaderAction-Objekt für die Erstellung des PSRulesEngineAction-Objekts.</span><span class="sxs-lookup"><span data-stu-id="92bb2-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="92bb2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="92bb2-107">EXAMPLES</span></span>

### <span data-ttu-id="92bb2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="92bb2-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="92bb2-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="92bb2-109">PARAMETERS</span></span>

### <span data-ttu-id="92bb2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92bb2-110">-DefaultProfile</span></span>
<span data-ttu-id="92bb2-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92bb2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92bb2-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="92bb2-112">-HeaderActionType</span></span>
<span data-ttu-id="92bb2-113">Welcher Manipulationstyp auf die Kopfzeile angewendet werden soll</span><span class="sxs-lookup"><span data-stu-id="92bb2-113">Which type of manipulation to apply to the header.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderActionType
Parameter Sets: (All)
Aliases:
Accepted values: Append, Delete, Overwrite

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bb2-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="92bb2-114">-HeaderName</span></span>
<span data-ttu-id="92bb2-115">Der Name der Kopfzeile, für die diese Aktion gilt.</span><span class="sxs-lookup"><span data-stu-id="92bb2-115">The name of the header this action will apply to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bb2-116">-Wert</span><span class="sxs-lookup"><span data-stu-id="92bb2-116">-Value</span></span>
<span data-ttu-id="92bb2-117">Der Wert, mit dem der angegebene Headername aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="92bb2-117">The value to update the given header name with.</span></span>
<span data-ttu-id="92bb2-118">Dieser Wert wird nicht verwendet, wenn der aktionTyp "Löschen" ist.</span><span class="sxs-lookup"><span data-stu-id="92bb2-118">This value is not used if the actionType is Delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bb2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92bb2-119">CommonParameters</span></span>
<span data-ttu-id="92bb2-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92bb2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92bb2-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92bb2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92bb2-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="92bb2-122">INPUTS</span></span>

### <span data-ttu-id="92bb2-123">Keine</span><span class="sxs-lookup"><span data-stu-id="92bb2-123">None</span></span>

## <span data-ttu-id="92bb2-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="92bb2-124">OUTPUTS</span></span>

### <span data-ttu-id="92bb2-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="92bb2-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="92bb2-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="92bb2-126">NOTES</span></span>

## <span data-ttu-id="92bb2-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="92bb2-127">RELATED LINKS</span></span>
