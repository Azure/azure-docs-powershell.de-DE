---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291400"
---
# <span data-ttu-id="d129e-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="d129e-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="d129e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d129e-102">SYNOPSIS</span></span>
<span data-ttu-id="d129e-103">Ruft die Access-Restiction-Konfiguration für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="d129e-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="d129e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d129e-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d129e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d129e-105">DESCRIPTION</span></span>
<span data-ttu-id="d129e-106">Das **Cmdlet "Get-AzWebAppAccessRestrictionConfig"** ruft die Zugriffseinschränkungskonfiguration für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="d129e-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="d129e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d129e-107">EXAMPLES</span></span>

### <span data-ttu-id="d129e-108">Beispiel 1: Erhalten einer Web App Access Restriction Config aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="d129e-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="d129e-109">Dieser Befehl ruft die Zugriffseinschränkungskonfiguration einer Web App namens "ContosoSite" ab, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="d129e-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d129e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d129e-110">PARAMETERS</span></span>

### <span data-ttu-id="d129e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d129e-111">-DefaultProfile</span></span>
<span data-ttu-id="d129e-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d129e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d129e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d129e-113">-Name</span></span>
<span data-ttu-id="d129e-114">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="d129e-114">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d129e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d129e-115">-ResourceGroupName</span></span>
<span data-ttu-id="d129e-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="d129e-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d129e-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="d129e-117">-SlotName</span></span>
<span data-ttu-id="d129e-118">Name des Bereitstellungsplatzes.</span><span class="sxs-lookup"><span data-stu-id="d129e-118">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d129e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d129e-119">CommonParameters</span></span>
<span data-ttu-id="d129e-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d129e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d129e-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d129e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d129e-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d129e-122">INPUTS</span></span>

### <span data-ttu-id="d129e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d129e-123">System.String</span></span>

## <span data-ttu-id="d129e-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d129e-124">OUTPUTS</span></span>

### <span data-ttu-id="d129e-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="d129e-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="d129e-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d129e-126">NOTES</span></span>

## <span data-ttu-id="d129e-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d129e-127">RELATED LINKS</span></span>

[<span data-ttu-id="d129e-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="d129e-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="d129e-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="d129e-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="d129e-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="d129e-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
