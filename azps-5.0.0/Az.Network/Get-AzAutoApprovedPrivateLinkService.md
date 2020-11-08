---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azautoapprovedprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAutoApprovedPrivateLinkService.md
ms.openlocfilehash: b03aad1f76c5151746d50e69bc48ccf10e60842f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180173"
---
# <span data-ttu-id="7ccea-101">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7ccea-101">Get-AzAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="7ccea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ccea-102">SYNOPSIS</span></span>
<span data-ttu-id="7ccea-103">Ruft ein Array privater Link Dienst-ID ab, das mit einem privaten Endpunkt mit automatisch genehmigt verknüpft werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ccea-103">Gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="7ccea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ccea-104">SYNTAX</span></span>

```
Get-AzAutoApprovedPrivateLinkService -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ccea-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ccea-105">DESCRIPTION</span></span>
<span data-ttu-id="7ccea-106">Der **Get-AzAutoApprovedPrivateLinkService** Ruft ein Array mit einer privaten Link Dienst-ID ab, die mit einem privaten Endpunkt mit automatisch genehmigt verknüpft werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ccea-106">The **Get-AzAutoApprovedPrivateLinkService** gets an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="7ccea-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ccea-107">EXAMPLES</span></span>

### <span data-ttu-id="7ccea-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7ccea-108">Example</span></span>
```
Get-AzAutoApprovedPrivateLinkService -Location westus -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="7ccea-109">In diesem Beispiel wird ein Array privater Link Dienst-ID zurückgegeben, das mit einem privaten Endpunkt mit automatisch genehmigt verknüpft werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ccea-109">This example return an array of private link service id that can be linked to a private end point with auto approved.</span></span>

## <span data-ttu-id="7ccea-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ccea-110">PARAMETERS</span></span>

### <span data-ttu-id="7ccea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ccea-111">-DefaultProfile</span></span>
<span data-ttu-id="7ccea-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7ccea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ccea-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="7ccea-113">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ccea-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ccea-114">-ResourceGroupName</span></span>
<span data-ttu-id="7ccea-115">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="7ccea-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7ccea-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ccea-116">CommonParameters</span></span>
<span data-ttu-id="7ccea-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ccea-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ccea-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ccea-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ccea-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ccea-119">INPUTS</span></span>

### <span data-ttu-id="7ccea-120">Keine</span><span class="sxs-lookup"><span data-stu-id="7ccea-120">None</span></span>

## <span data-ttu-id="7ccea-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ccea-121">OUTPUTS</span></span>

### <span data-ttu-id="7ccea-122">Microsoft. Azure. Commands. Network. Models. PSAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7ccea-122">Microsoft.Azure.Commands.Network.Models.PSAutoApprovedPrivateLinkService</span></span>

## <span data-ttu-id="7ccea-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ccea-123">NOTES</span></span>

## <span data-ttu-id="7ccea-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ccea-124">RELATED LINKS</span></span>
