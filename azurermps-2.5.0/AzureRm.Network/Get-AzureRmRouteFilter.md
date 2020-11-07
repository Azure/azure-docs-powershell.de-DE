---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 007f020d97d0c46f5db5031f4163d669d976f642
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850687"
---
# <span data-ttu-id="9ef66-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9ef66-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="9ef66-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ef66-102">SYNOPSIS</span></span>
<span data-ttu-id="9ef66-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="9ef66-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ef66-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ef66-104">SYNTAX</span></span>

### <span data-ttu-id="9ef66-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="9ef66-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ef66-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="9ef66-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ef66-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ef66-107">DESCRIPTION</span></span>
<span data-ttu-id="9ef66-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="9ef66-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="9ef66-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ef66-109">EXAMPLES</span></span>

### <span data-ttu-id="9ef66-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9ef66-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9ef66-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="9ef66-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="9ef66-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ef66-112">PARAMETERS</span></span>

### <span data-ttu-id="9ef66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ef66-113">-DefaultProfile</span></span>
<span data-ttu-id="9ef66-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ef66-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ef66-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="9ef66-115">-ExpandResource</span></span>
<span data-ttu-id="9ef66-116">Der Ressourcenverweis, der erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9ef66-116">The resource reference to be expanded.</span></span>

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ef66-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9ef66-117">-Name</span></span>
<span data-ttu-id="9ef66-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="9ef66-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ef66-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ef66-119">-ResourceGroupName</span></span>
<span data-ttu-id="9ef66-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9ef66-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ef66-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ef66-121">CommonParameters</span></span>
<span data-ttu-id="9ef66-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ef66-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ef66-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ef66-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ef66-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ef66-124">INPUTS</span></span>

### <span data-ttu-id="9ef66-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9ef66-125">System.String</span></span>

## <span data-ttu-id="9ef66-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ef66-126">OUTPUTS</span></span>

### <span data-ttu-id="9ef66-127">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9ef66-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9ef66-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ef66-128">NOTES</span></span>

## <span data-ttu-id="9ef66-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ef66-129">RELATED LINKS</span></span>

