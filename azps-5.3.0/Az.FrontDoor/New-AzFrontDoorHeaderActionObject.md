---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469787"
---
# <span data-ttu-id="10054-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="10054-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="10054-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10054-102">SYNOPSIS</span></span>
<span data-ttu-id="10054-103">Erstellen Sie ein PSHeaderAction-Objekt.</span><span class="sxs-lookup"><span data-stu-id="10054-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="10054-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10054-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10054-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10054-105">DESCRIPTION</span></span>
<span data-ttu-id="10054-106">Erstellt ein PSHeaderAction-Objekt für die Erstellung des PSRulesEngineAction-Objekts.</span><span class="sxs-lookup"><span data-stu-id="10054-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="10054-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="10054-107">EXAMPLES</span></span>

### <span data-ttu-id="10054-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10054-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="10054-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10054-109">PARAMETERS</span></span>

### <span data-ttu-id="10054-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10054-110">-DefaultProfile</span></span>
<span data-ttu-id="10054-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10054-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10054-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="10054-112">-HeaderActionType</span></span>
<span data-ttu-id="10054-113">Welche Art von Manipulation soll auf die Kopfzeile angewendet werden?</span><span class="sxs-lookup"><span data-stu-id="10054-113">Which type of manipulation to apply to the header.</span></span>

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

### <span data-ttu-id="10054-114">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="10054-114">-HeaderName</span></span>
<span data-ttu-id="10054-115">Der Name der Kopfzeile, für die diese Aktion gilt.</span><span class="sxs-lookup"><span data-stu-id="10054-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="10054-116">-Value</span><span class="sxs-lookup"><span data-stu-id="10054-116">-Value</span></span>
<span data-ttu-id="10054-117">Der Wert, mit dem der angegebene Headername aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="10054-117">The value to update the given header name with.</span></span>
<span data-ttu-id="10054-118">Dieser Wert wird nicht verwendet, wenn "actionType" "Delete" ist.</span><span class="sxs-lookup"><span data-stu-id="10054-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="10054-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10054-119">CommonParameters</span></span>
<span data-ttu-id="10054-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10054-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10054-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10054-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10054-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="10054-122">INPUTS</span></span>

### <span data-ttu-id="10054-123">Keine</span><span class="sxs-lookup"><span data-stu-id="10054-123">None</span></span>

## <span data-ttu-id="10054-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="10054-124">OUTPUTS</span></span>

### <span data-ttu-id="10054-125">Microsoft.Azure.Commands.FrontD selbst.Models.PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="10054-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="10054-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="10054-126">NOTES</span></span>

## <span data-ttu-id="10054-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="10054-127">RELATED LINKS</span></span>
