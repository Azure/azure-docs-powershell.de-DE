---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzRouteFilter.md
ms.openlocfilehash: 1d914509b43dd59d95d32a11c3f5ce3487b03e7a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841528"
---
# <span data-ttu-id="42b9d-101">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="42b9d-101">Get-AzRouteFilter</span></span>

## <span data-ttu-id="42b9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="42b9d-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="42b9d-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="42b9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42b9d-104">SYNTAX</span></span>

### <span data-ttu-id="42b9d-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="42b9d-105">NoExpand</span></span>
```
Get-AzRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42b9d-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="42b9d-106">Expand</span></span>
```
Get-AzRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42b9d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42b9d-107">DESCRIPTION</span></span>
<span data-ttu-id="42b9d-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="42b9d-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="42b9d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42b9d-109">EXAMPLES</span></span>

### <span data-ttu-id="42b9d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="42b9d-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="42b9d-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="42b9d-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="42b9d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="42b9d-112">PARAMETERS</span></span>

### <span data-ttu-id="42b9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42b9d-113">-DefaultProfile</span></span>
<span data-ttu-id="42b9d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42b9d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42b9d-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="42b9d-115">-ExpandResource</span></span>
<span data-ttu-id="42b9d-116">Der Ressourcenverweis, der erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="42b9d-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="42b9d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="42b9d-117">-Name</span></span>
<span data-ttu-id="42b9d-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="42b9d-118">The resource name.</span></span>

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

### <span data-ttu-id="42b9d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42b9d-119">-ResourceGroupName</span></span>
<span data-ttu-id="42b9d-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="42b9d-120">The resource group name.</span></span>

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

### <span data-ttu-id="42b9d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b9d-121">CommonParameters</span></span>
<span data-ttu-id="42b9d-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b9d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b9d-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42b9d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b9d-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42b9d-124">INPUTS</span></span>

### <span data-ttu-id="42b9d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="42b9d-125">System.String</span></span>

## <span data-ttu-id="42b9d-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42b9d-126">OUTPUTS</span></span>

### <span data-ttu-id="42b9d-127">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="42b9d-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="42b9d-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="42b9d-128">NOTES</span></span>

## <span data-ttu-id="42b9d-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42b9d-129">RELATED LINKS</span></span>

