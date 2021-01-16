---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367113"
---
# <span data-ttu-id="3f08c-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3f08c-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="3f08c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f08c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f08c-103">Erhalten Sie eine Routingregel für den angegebenen Slotnamen.</span><span class="sxs-lookup"><span data-stu-id="3f08c-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="3f08c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f08c-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f08c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f08c-105">DESCRIPTION</span></span>
<span data-ttu-id="3f08c-106">Das **Cmdlet "Get-AzWebAppTrafficRouting"** ruft eine Routingregelkonfiguration aus einem Azure Web App-Slot ab.</span><span class="sxs-lookup"><span data-stu-id="3f08c-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="3f08c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f08c-107">EXAMPLES</span></span>

### <span data-ttu-id="3f08c-108">Beispiel 1 Ruft die spezifische Routingregel vom Webappplatz ab</span><span class="sxs-lookup"><span data-stu-id="3f08c-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="3f08c-109">Dieser Befehl ruft eine Routingregel für einen bestimmten WebApp-Slot ab.</span><span class="sxs-lookup"><span data-stu-id="3f08c-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="3f08c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f08c-110">PARAMETERS</span></span>

### <span data-ttu-id="3f08c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f08c-111">-DefaultProfile</span></span>
<span data-ttu-id="3f08c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f08c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f08c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f08c-113">-ResourceGroupName</span></span>
<span data-ttu-id="3f08c-114">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="3f08c-114">Resource Group Name</span></span>

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

### <span data-ttu-id="3f08c-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="3f08c-115">-RuleName</span></span>
<span data-ttu-id="3f08c-116">Regelname</span><span class="sxs-lookup"><span data-stu-id="3f08c-116">Rule Name</span></span>
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

### <span data-ttu-id="3f08c-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="3f08c-117">-WebAppName</span></span>
<span data-ttu-id="3f08c-118">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="3f08c-118">WebApp Name</span></span>

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

### <span data-ttu-id="3f08c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f08c-119">CommonParameters</span></span>
<span data-ttu-id="3f08c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f08c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f08c-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f08c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f08c-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f08c-122">INPUTS</span></span>

### <span data-ttu-id="3f08c-123">Keine</span><span class="sxs-lookup"><span data-stu-id="3f08c-123">None</span></span>

## <span data-ttu-id="3f08c-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f08c-124">OUTPUTS</span></span>

### <span data-ttu-id="3f08c-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="3f08c-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="3f08c-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3f08c-126">NOTES</span></span>

## <span data-ttu-id="3f08c-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3f08c-127">RELATED LINKS</span></span>

[<span data-ttu-id="3f08c-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3f08c-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="3f08c-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3f08c-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="3f08c-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="3f08c-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
