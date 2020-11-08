---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorheaderactionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHeaderActionObject.md
ms.openlocfilehash: e718fbf4c46c69e5076ab95311aedb54132b604f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177623"
---
# <span data-ttu-id="d9d7d-101">New-AzFrontDoorHeaderActionObject</span><span class="sxs-lookup"><span data-stu-id="d9d7d-101">New-AzFrontDoorHeaderActionObject</span></span>

## <span data-ttu-id="d9d7d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9d7d-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d7d-103">Erstellen Sie ein PSHeaderAction-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d9d7d-103">Create PSHeaderAction object.</span></span>

## <span data-ttu-id="d9d7d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9d7d-104">SYNTAX</span></span>

```
New-AzFrontDoorHeaderActionObject -HeaderName <String> -HeaderActionType <PSHeaderActionType> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9d7d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9d7d-105">DESCRIPTION</span></span>
<span data-ttu-id="d9d7d-106">Erstellt ein PSHeaderAction-Objekt für die Erstellung des PSRulesEngineAction-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d9d7d-106">Creates PSHeaderAction object for the creation of PSRulesEngineAction object.</span></span>

## <span data-ttu-id="d9d7d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9d7d-107">EXAMPLES</span></span>

### <span data-ttu-id="d9d7d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d9d7d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorHeaderActionObject -HeaderName headername -HeaderActionType Append

HeaderName HeaderActionType Value
---------- ---------------- -----
headername           Append
```

## <span data-ttu-id="d9d7d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9d7d-109">PARAMETERS</span></span>

### <span data-ttu-id="d9d7d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d7d-110">-DefaultProfile</span></span>
<span data-ttu-id="d9d7d-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9d7d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9d7d-112">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="d9d7d-112">-HeaderActionType</span></span>
<span data-ttu-id="d9d7d-113">Welche Art von Manipulation auf die Kopfzeile angewendet werden soll</span><span class="sxs-lookup"><span data-stu-id="d9d7d-113">Which type of manipulation to apply to the header.</span></span>

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

### <span data-ttu-id="d9d7d-114">-Headername</span><span class="sxs-lookup"><span data-stu-id="d9d7d-114">-HeaderName</span></span>
<span data-ttu-id="d9d7d-115">Der Name des Headers, auf den diese Aktion angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9d7d-115">The name of the header this action will apply to.</span></span>

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

### <span data-ttu-id="d9d7d-116">-Wert</span><span class="sxs-lookup"><span data-stu-id="d9d7d-116">-Value</span></span>
<span data-ttu-id="d9d7d-117">Der Wert, mit dem der angegebene Headername aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9d7d-117">The value to update the given header name with.</span></span>
<span data-ttu-id="d9d7d-118">Dieser Wert wird nicht verwendet, wenn es sich bei dem ActionType um DELETE handelt.</span><span class="sxs-lookup"><span data-stu-id="d9d7d-118">This value is not used if the actionType is Delete.</span></span>

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

### <span data-ttu-id="d9d7d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d7d-119">CommonParameters</span></span>
<span data-ttu-id="d9d7d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9d7d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d7d-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9d7d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d7d-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9d7d-122">INPUTS</span></span>

### <span data-ttu-id="d9d7d-123">Keine</span><span class="sxs-lookup"><span data-stu-id="d9d7d-123">None</span></span>

## <span data-ttu-id="d9d7d-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9d7d-124">OUTPUTS</span></span>

### <span data-ttu-id="d9d7d-125">Microsoft. Azure. Commands. Haustür. Models. PSHeaderAction</span><span class="sxs-lookup"><span data-stu-id="d9d7d-125">Microsoft.Azure.Commands.FrontDoor.Models.PSHeaderAction</span></span>

## <span data-ttu-id="d9d7d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9d7d-126">NOTES</span></span>

## <span data-ttu-id="d9d7d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9d7d-127">RELATED LINKS</span></span>
