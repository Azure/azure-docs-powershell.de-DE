---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: faa3264dbf9fa65a2970f578c635868d185f2ef8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174732"
---
# <span data-ttu-id="06ff5-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="06ff5-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="06ff5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06ff5-102">SYNOPSIS</span></span>
<span data-ttu-id="06ff5-103">Startet eine Azure Web App neu.</span><span class="sxs-lookup"><span data-stu-id="06ff5-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="06ff5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06ff5-104">SYNTAX</span></span>

### <span data-ttu-id="06ff5-105">S1</span><span class="sxs-lookup"><span data-stu-id="06ff5-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06ff5-106">S2</span><span class="sxs-lookup"><span data-stu-id="06ff5-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06ff5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06ff5-107">DESCRIPTION</span></span>
<span data-ttu-id="06ff5-108">Das **Cmdlet "Restart-AzWebApp"** wird beendet und dann eine Azure Web App gestartet.</span><span class="sxs-lookup"><span data-stu-id="06ff5-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="06ff5-109">Wenn sich die Web App im angehaltenen Zustand befindet, verwenden Sie das Start-AzWebApp-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06ff5-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="06ff5-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="06ff5-110">EXAMPLES</span></span>

### <span data-ttu-id="06ff5-111">Beispiel 1: Neustarten einer Web App</span><span class="sxs-lookup"><span data-stu-id="06ff5-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="06ff5-112">Mit diesem Befehl wird die Azure Web App namens "ContosoSite" beendet, die zur Ressourcengruppe "Default-Web-WestUS" gehört, und dann neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="06ff5-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="06ff5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06ff5-113">PARAMETERS</span></span>

### <span data-ttu-id="06ff5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ff5-114">-DefaultProfile</span></span>
<span data-ttu-id="06ff5-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06ff5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06ff5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="06ff5-116">-Name</span></span>
<span data-ttu-id="06ff5-117">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="06ff5-117">WebApp Name</span></span>

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

### <span data-ttu-id="06ff5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06ff5-118">-ResourceGroupName</span></span>
<span data-ttu-id="06ff5-119">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="06ff5-119">Resource Group Name</span></span>

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

### <span data-ttu-id="06ff5-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="06ff5-120">-WebApp</span></span>
<span data-ttu-id="06ff5-121">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="06ff5-121">WebApp Object</span></span>

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

### <span data-ttu-id="06ff5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ff5-122">CommonParameters</span></span>
<span data-ttu-id="06ff5-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06ff5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ff5-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06ff5-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ff5-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="06ff5-125">INPUTS</span></span>

### <span data-ttu-id="06ff5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="06ff5-126">System.String</span></span>

### <span data-ttu-id="06ff5-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="06ff5-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="06ff5-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="06ff5-128">OUTPUTS</span></span>

### <span data-ttu-id="06ff5-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="06ff5-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="06ff5-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="06ff5-130">NOTES</span></span>

## <span data-ttu-id="06ff5-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="06ff5-131">RELATED LINKS</span></span>

[<span data-ttu-id="06ff5-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="06ff5-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="06ff5-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="06ff5-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="06ff5-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="06ff5-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="06ff5-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="06ff5-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="06ff5-136">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="06ff5-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


