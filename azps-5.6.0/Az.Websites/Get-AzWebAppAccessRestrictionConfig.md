---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934531"
---
# <span data-ttu-id="6cb21-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="6cb21-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="6cb21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cb21-102">SYNOPSIS</span></span>
<span data-ttu-id="6cb21-103">Ruft die Access Restiction-Konfiguration für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="6cb21-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="6cb21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cb21-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6cb21-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6cb21-105">DESCRIPTION</span></span>
<span data-ttu-id="6cb21-106">Das **Get-AzWebAppAccessRestrictionConfig-Cmdlet** ruft die Zugriffseinschränkungskonfiguration für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="6cb21-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="6cb21-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6cb21-107">EXAMPLES</span></span>

### <span data-ttu-id="6cb21-108">Beispiel 1: Herunterladen einer Web App Access Restriction Config aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6cb21-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="6cb21-109">Dieser Befehl ruft die Zugriffseinschränkungskonfiguration einer Web App namens ContosoSite ab, die zur Ressourcengruppe Default-Web-WestUS gehört.</span><span class="sxs-lookup"><span data-stu-id="6cb21-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6cb21-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6cb21-110">PARAMETERS</span></span>

### <span data-ttu-id="6cb21-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cb21-111">-DefaultProfile</span></span>
<span data-ttu-id="6cb21-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6cb21-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cb21-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6cb21-113">-Name</span></span>
<span data-ttu-id="6cb21-114">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="6cb21-114">WebApp Name</span></span>

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

### <span data-ttu-id="6cb21-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cb21-115">-ResourceGroupName</span></span>
<span data-ttu-id="6cb21-116">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="6cb21-116">Resource Group Name</span></span>

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

### <span data-ttu-id="6cb21-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="6cb21-117">-SlotName</span></span>
<span data-ttu-id="6cb21-118">Name des Bereitstellungsplatzes.</span><span class="sxs-lookup"><span data-stu-id="6cb21-118">Deployment Slot name.</span></span>

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

### <span data-ttu-id="6cb21-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cb21-119">CommonParameters</span></span>
<span data-ttu-id="6cb21-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cb21-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cb21-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6cb21-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cb21-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6cb21-122">INPUTS</span></span>

### <span data-ttu-id="6cb21-123">System.String</span><span class="sxs-lookup"><span data-stu-id="6cb21-123">System.String</span></span>

## <span data-ttu-id="6cb21-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6cb21-124">OUTPUTS</span></span>

### <span data-ttu-id="6cb21-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="6cb21-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="6cb21-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6cb21-126">NOTES</span></span>

## <span data-ttu-id="6cb21-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6cb21-127">RELATED LINKS</span></span>

[<span data-ttu-id="6cb21-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="6cb21-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="6cb21-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="6cb21-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="6cb21-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="6cb21-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
