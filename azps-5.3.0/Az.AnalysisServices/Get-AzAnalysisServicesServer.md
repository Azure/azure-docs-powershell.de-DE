---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/get-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Get-AzAnalysisServicesServer.md
ms.openlocfilehash: c0c308bfe9d2d5fad971f9df1a26b03710d5629c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469072"
---
# <span data-ttu-id="0da3b-101">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0da3b-101">Get-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="0da3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0da3b-102">SYNOPSIS</span></span>
<span data-ttu-id="0da3b-103">Ruft die Details eines Analysis Services-Servers ab.</span><span class="sxs-lookup"><span data-stu-id="0da3b-103">Gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="0da3b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0da3b-104">SYNTAX</span></span>

```
Get-AzAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0da3b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0da3b-105">DESCRIPTION</span></span>
<span data-ttu-id="0da3b-106">Das Get-AzAnalysisServicesServer cmdlet ruft die Details eines Analysis Services-Servers ab.</span><span class="sxs-lookup"><span data-stu-id="0da3b-106">The Get-AzAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="0da3b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0da3b-107">EXAMPLES</span></span>

### <span data-ttu-id="0da3b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0da3b-108">Example 1</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="0da3b-109">Dieser Befehl ruft alle Azure Analysis Services-Server in der Ressourcengruppe mit dem Namen "ResourceGroup03" ab.</span><span class="sxs-lookup"><span data-stu-id="0da3b-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="0da3b-110">Beispiel 2: Server erhalten</span><span class="sxs-lookup"><span data-stu-id="0da3b-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="0da3b-111">Dieser Befehl ruft den Azure Analysis Services-Server namens "Testserver" in der Ressourcengruppe mit dem Namen "ResourceGroup03" ab.</span><span class="sxs-lookup"><span data-stu-id="0da3b-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="0da3b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0da3b-112">PARAMETERS</span></span>

### <span data-ttu-id="0da3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da3b-113">-DefaultProfile</span></span>
<span data-ttu-id="0da3b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0da3b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0da3b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0da3b-115">-Name</span></span>
<span data-ttu-id="0da3b-116">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="0da3b-116">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0da3b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0da3b-117">-ResourceGroupName</span></span>
<span data-ttu-id="0da3b-118">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="0da3b-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0da3b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da3b-119">CommonParameters</span></span>
<span data-ttu-id="0da3b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0da3b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da3b-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0da3b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da3b-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0da3b-122">INPUTS</span></span>

### <span data-ttu-id="0da3b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0da3b-123">System.String</span></span>

## <span data-ttu-id="0da3b-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0da3b-124">OUTPUTS</span></span>

### <span data-ttu-id="0da3b-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="0da3b-125">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="0da3b-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0da3b-126">NOTES</span></span>
<span data-ttu-id="0da3b-127">Alias: Get-AzAs</span><span class="sxs-lookup"><span data-stu-id="0da3b-127">Alias: Get-AzAs</span></span>

## <span data-ttu-id="0da3b-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0da3b-128">RELATED LINKS</span></span>

[<span data-ttu-id="0da3b-129">New-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="0da3b-129">New-AzAnalysisServicesServer </span></span>](./New-AzAnalysisServicesServer .md)

[<span data-ttu-id="0da3b-130">Remove-AzAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="0da3b-130">Remove-AzAnalysisServicesServer </span></span>](./Remove-AzAnalysisServicesServer .md)
