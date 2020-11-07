---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845747"
---
# <span data-ttu-id="131b2-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="131b2-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="131b2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="131b2-102">SYNOPSIS</span></span>
<span data-ttu-id="131b2-103">Get-AzWebAppContainerContinuousDeploymentUrl gibt die URL der fortlaufenden Container Bereitstellung zurück</span><span class="sxs-lookup"><span data-stu-id="131b2-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="131b2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="131b2-104">SYNTAX</span></span>

### <span data-ttu-id="131b2-105">S1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="131b2-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="131b2-106">S2</span><span class="sxs-lookup"><span data-stu-id="131b2-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="131b2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="131b2-107">DESCRIPTION</span></span>
<span data-ttu-id="131b2-108">Get-AzWebAppContainerContinuousDeploymentUrl gibt die URL der fortlaufenden Container Bereitstellung zurück</span><span class="sxs-lookup"><span data-stu-id="131b2-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="131b2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="131b2-109">EXAMPLES</span></span>

### <span data-ttu-id="131b2-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="131b2-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="131b2-111">Dieser Befehl gibt die Container-URL für die fortlaufende Bereitstellung zurück.</span><span class="sxs-lookup"><span data-stu-id="131b2-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="131b2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="131b2-112">PARAMETERS</span></span>

### <span data-ttu-id="131b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="131b2-113">-DefaultProfile</span></span>
<span data-ttu-id="131b2-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="131b2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="131b2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="131b2-115">-Name</span></span>
<span data-ttu-id="131b2-116">Der Name der Web-App.</span><span class="sxs-lookup"><span data-stu-id="131b2-116">The name of the web app.</span></span>

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

### <span data-ttu-id="131b2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="131b2-117">-ResourceGroupName</span></span>
<span data-ttu-id="131b2-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="131b2-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="131b2-119">-Slotname</span><span class="sxs-lookup"><span data-stu-id="131b2-119">-SlotName</span></span>
<span data-ttu-id="131b2-120">Der Name des Web App-Slots.</span><span class="sxs-lookup"><span data-stu-id="131b2-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="131b2-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="131b2-121">-WebApp</span></span>
<span data-ttu-id="131b2-122">Das Web App-Objekt</span><span class="sxs-lookup"><span data-stu-id="131b2-122">The web app object</span></span>

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

### <span data-ttu-id="131b2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131b2-123">CommonParameters</span></span>
<span data-ttu-id="131b2-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="131b2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131b2-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="131b2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131b2-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="131b2-126">INPUTS</span></span>

### <span data-ttu-id="131b2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="131b2-127">System.String</span></span>

### <span data-ttu-id="131b2-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="131b2-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="131b2-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="131b2-129">OUTPUTS</span></span>

### <span data-ttu-id="131b2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="131b2-130">System.String</span></span>

## <span data-ttu-id="131b2-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="131b2-131">NOTES</span></span>

## <span data-ttu-id="131b2-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="131b2-132">RELATED LINKS</span></span>
