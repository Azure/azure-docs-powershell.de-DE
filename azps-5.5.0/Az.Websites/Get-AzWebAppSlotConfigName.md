---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 9ca0578aacbd0ca970211bc38419880cbe99675b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173412"
---
# <span data-ttu-id="7850b-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="7850b-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="7850b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7850b-102">SYNOPSIS</span></span>
<span data-ttu-id="7850b-103">Liste der Web App-Slot-Konfigurationsnamen</span><span class="sxs-lookup"><span data-stu-id="7850b-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="7850b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7850b-104">SYNTAX</span></span>

### <span data-ttu-id="7850b-105">S1</span><span class="sxs-lookup"><span data-stu-id="7850b-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7850b-106">S2</span><span class="sxs-lookup"><span data-stu-id="7850b-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7850b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7850b-107">DESCRIPTION</span></span>
<span data-ttu-id="7850b-108">Das **Cmdlet "Get-AzWebAppSlotConfigName"** ruft die Liste der Namen von "App-Einstellung" und "Verbindungszeichenfolge" ab, die derzeit als Sloteinstellungen markiert sind.</span><span class="sxs-lookup"><span data-stu-id="7850b-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="7850b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7850b-109">EXAMPLES</span></span>

### <span data-ttu-id="7850b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7850b-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="7850b-111">Dieser Befehl ruft Die App-Einstellungen und Verbindungszeichenfolgen ab, die sich auf die Web App namens "ContosoSite" bezieht, die der Ressourcengruppe "Default-Web-WestUS" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7850b-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="7850b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7850b-112">PARAMETERS</span></span>

### <span data-ttu-id="7850b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7850b-113">-DefaultProfile</span></span>
<span data-ttu-id="7850b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7850b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7850b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7850b-115">-Name</span></span>
<span data-ttu-id="7850b-116">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="7850b-116">WebApp Name</span></span>

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

### <span data-ttu-id="7850b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7850b-117">-ResourceGroupName</span></span>
<span data-ttu-id="7850b-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="7850b-118">Resource Group Name</span></span>

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

### <span data-ttu-id="7850b-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7850b-119">-WebApp</span></span>
<span data-ttu-id="7850b-120">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="7850b-120">WebApp Object</span></span>

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

### <span data-ttu-id="7850b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7850b-121">CommonParameters</span></span>
<span data-ttu-id="7850b-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7850b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7850b-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7850b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7850b-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7850b-124">INPUTS</span></span>

### <span data-ttu-id="7850b-125">System.String</span><span class="sxs-lookup"><span data-stu-id="7850b-125">System.String</span></span>

### <span data-ttu-id="7850b-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="7850b-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7850b-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7850b-127">OUTPUTS</span></span>

### <span data-ttu-id="7850b-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="7850b-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="7850b-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7850b-129">NOTES</span></span>

## <span data-ttu-id="7850b-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7850b-130">RELATED LINKS</span></span>
