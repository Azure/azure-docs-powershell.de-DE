---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165436"
---
# <span data-ttu-id="808ac-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="808ac-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="808ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="808ac-102">SYNOPSIS</span></span>
<span data-ttu-id="808ac-103">Get-AzWebAppContainerContinuousDeploymentUrl gibt die fortlaufende Bereitstellungs-URL des Containers zurück.</span><span class="sxs-lookup"><span data-stu-id="808ac-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="808ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="808ac-104">SYNTAX</span></span>

### <span data-ttu-id="808ac-105">S1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="808ac-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="808ac-106">S2</span><span class="sxs-lookup"><span data-stu-id="808ac-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="808ac-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="808ac-107">DESCRIPTION</span></span>
<span data-ttu-id="808ac-108">Get-AzWebAppContainerContinuousDeploymentUrl gibt die fortlaufende Bereitstellungs-URL des Containers zurück.</span><span class="sxs-lookup"><span data-stu-id="808ac-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="808ac-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="808ac-109">EXAMPLES</span></span>

### <span data-ttu-id="808ac-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="808ac-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="808ac-111">Dieser Befehl gibt die Container-URL für fortlaufende Bereitstellung zurück.</span><span class="sxs-lookup"><span data-stu-id="808ac-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="808ac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="808ac-112">PARAMETERS</span></span>

### <span data-ttu-id="808ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808ac-113">-DefaultProfile</span></span>
<span data-ttu-id="808ac-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="808ac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="808ac-115">-Name</span><span class="sxs-lookup"><span data-stu-id="808ac-115">-Name</span></span>
<span data-ttu-id="808ac-116">Der Name der Web App.</span><span class="sxs-lookup"><span data-stu-id="808ac-116">The name of the web app.</span></span>

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

### <span data-ttu-id="808ac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="808ac-117">-ResourceGroupName</span></span>
<span data-ttu-id="808ac-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="808ac-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="808ac-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="808ac-119">-SlotName</span></span>
<span data-ttu-id="808ac-120">Der Name des Web-App-Slot.</span><span class="sxs-lookup"><span data-stu-id="808ac-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="808ac-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="808ac-121">-WebApp</span></span>
<span data-ttu-id="808ac-122">Web -App-Objekt</span><span class="sxs-lookup"><span data-stu-id="808ac-122">The web app object</span></span>

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

### <span data-ttu-id="808ac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808ac-123">CommonParameters</span></span>
<span data-ttu-id="808ac-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="808ac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808ac-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="808ac-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808ac-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="808ac-126">INPUTS</span></span>

### <span data-ttu-id="808ac-127">System.String</span><span class="sxs-lookup"><span data-stu-id="808ac-127">System.String</span></span>

### <span data-ttu-id="808ac-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="808ac-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="808ac-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="808ac-129">OUTPUTS</span></span>

### <span data-ttu-id="808ac-130">System.String</span><span class="sxs-lookup"><span data-stu-id="808ac-130">System.String</span></span>

## <span data-ttu-id="808ac-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="808ac-131">NOTES</span></span>

## <span data-ttu-id="808ac-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="808ac-132">RELATED LINKS</span></span>
