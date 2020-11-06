---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilter.md
ms.openlocfilehash: 2c980b981679ddfa3fb2eda473b495f9281c227d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479725"
---
# <span data-ttu-id="6b261-101">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6b261-101">Get-AzureRmRouteFilter</span></span>

## <span data-ttu-id="6b261-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b261-102">SYNOPSIS</span></span>
<span data-ttu-id="6b261-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="6b261-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b261-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b261-104">SYNTAX</span></span>

### <span data-ttu-id="6b261-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="6b261-105">NoExpand</span></span>
```
Get-AzureRmRouteFilter [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b261-106">Erweitern</span><span class="sxs-lookup"><span data-stu-id="6b261-106">Expand</span></span>
```
Get-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b261-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b261-107">DESCRIPTION</span></span>
<span data-ttu-id="6b261-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="6b261-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="6b261-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b261-109">EXAMPLES</span></span>

### <span data-ttu-id="6b261-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6b261-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="6b261-111">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="6b261-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="6b261-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b261-112">PARAMETERS</span></span>

### <span data-ttu-id="6b261-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b261-113">-DefaultProfile</span></span>
<span data-ttu-id="6b261-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6b261-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b261-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="6b261-115">-ExpandResource</span></span>
<span data-ttu-id="6b261-116">Der Ressourcenverweis, der erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b261-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="6b261-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6b261-117">-Name</span></span>
<span data-ttu-id="6b261-118">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="6b261-118">The resource name.</span></span>

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

### <span data-ttu-id="6b261-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b261-119">-ResourceGroupName</span></span>
<span data-ttu-id="6b261-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6b261-120">The resource group name.</span></span>

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

### <span data-ttu-id="6b261-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b261-121">CommonParameters</span></span>
<span data-ttu-id="6b261-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b261-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b261-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b261-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b261-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b261-124">INPUTS</span></span>

### <span data-ttu-id="6b261-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6b261-125">System.String</span></span>

## <span data-ttu-id="6b261-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b261-126">OUTPUTS</span></span>

### <span data-ttu-id="6b261-127">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="6b261-127">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="6b261-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b261-128">NOTES</span></span>

## <span data-ttu-id="6b261-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b261-129">RELATED LINKS</span></span>

