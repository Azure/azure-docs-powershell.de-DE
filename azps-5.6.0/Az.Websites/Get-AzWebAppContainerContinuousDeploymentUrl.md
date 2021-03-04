---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 90aca2939721144500519329492e04786b67a93a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933491"
---
# <span data-ttu-id="ffc9e-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="ffc9e-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="ffc9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffc9e-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc9e-103">Get-AzWebAppContainerContinuousDeploymentUrl gibt die permanente Containerbereitstellungs-URL zurück.</span><span class="sxs-lookup"><span data-stu-id="ffc9e-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="ffc9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffc9e-104">SYNTAX</span></span>

### <span data-ttu-id="ffc9e-105">S1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="ffc9e-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffc9e-106">S2</span><span class="sxs-lookup"><span data-stu-id="ffc9e-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ffc9e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ffc9e-107">DESCRIPTION</span></span>
<span data-ttu-id="ffc9e-108">Get-AzWebAppContainerContinuousDeploymentUrl gibt die permanente Containerbereitstellungs-URL zurück.</span><span class="sxs-lookup"><span data-stu-id="ffc9e-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="ffc9e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ffc9e-109">EXAMPLES</span></span>

### <span data-ttu-id="ffc9e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ffc9e-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="ffc9e-111">Dieser Befehl gibt die url für die kontinuierliche Containerbereitstellung zurück.</span><span class="sxs-lookup"><span data-stu-id="ffc9e-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="ffc9e-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ffc9e-112">PARAMETERS</span></span>

### <span data-ttu-id="ffc9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc9e-113">-DefaultProfile</span></span>
<span data-ttu-id="ffc9e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ffc9e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffc9e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ffc9e-115">-Name</span></span>
<span data-ttu-id="ffc9e-116">Der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="ffc9e-116">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc9e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc9e-117">-ResourceGroupName</span></span>
<span data-ttu-id="ffc9e-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ffc9e-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc9e-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="ffc9e-119">-SlotName</span></span>
<span data-ttu-id="ffc9e-120">Der Name des Web-App-Steckplatzes.</span><span class="sxs-lookup"><span data-stu-id="ffc9e-120">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc9e-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ffc9e-121">-WebApp</span></span>
<span data-ttu-id="ffc9e-122">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="ffc9e-122">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc9e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc9e-123">CommonParameters</span></span>
<span data-ttu-id="ffc9e-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffc9e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc9e-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffc9e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc9e-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ffc9e-126">INPUTS</span></span>

### <span data-ttu-id="ffc9e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ffc9e-127">System.String</span></span>

### <span data-ttu-id="ffc9e-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ffc9e-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ffc9e-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ffc9e-129">OUTPUTS</span></span>

### <span data-ttu-id="ffc9e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ffc9e-130">System.String</span></span>

## <span data-ttu-id="ffc9e-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ffc9e-131">NOTES</span></span>

## <span data-ttu-id="ffc9e-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ffc9e-132">RELATED LINKS</span></span>
