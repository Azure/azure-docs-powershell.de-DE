---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 2157c7a570f38838a65e1d4bba40dade22e10367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923899"
---
# <span data-ttu-id="eda46-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="eda46-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="eda46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eda46-102">SYNOPSIS</span></span>
<span data-ttu-id="eda46-103">Liste der Web App Slot Config-Namen</span><span class="sxs-lookup"><span data-stu-id="eda46-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="eda46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eda46-104">SYNTAX</span></span>

### <span data-ttu-id="eda46-105">S1</span><span class="sxs-lookup"><span data-stu-id="eda46-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eda46-106">S2</span><span class="sxs-lookup"><span data-stu-id="eda46-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eda46-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eda46-107">DESCRIPTION</span></span>
<span data-ttu-id="eda46-108">Das **Get-AzWebAppSlotConfigName-Cmdlet** ruft die Liste der App-Einstellungs- und Verbindungszeichenfolgennamen ab, die derzeit als Sloteinstellungen gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="eda46-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="eda46-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eda46-109">EXAMPLES</span></span>

### <span data-ttu-id="eda46-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="eda46-110">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="eda46-111">Dieser Befehl ruft App-Einstellungen und Verbindungszeichenfolgen ab, die sich auf die Web App mit dem Namen ContosoSite bezieht, die der Ressourcengruppe Default-Web-WestUS zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="eda46-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="eda46-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eda46-112">PARAMETERS</span></span>

### <span data-ttu-id="eda46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eda46-113">-DefaultProfile</span></span>
<span data-ttu-id="eda46-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eda46-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eda46-115">-Name</span><span class="sxs-lookup"><span data-stu-id="eda46-115">-Name</span></span>
<span data-ttu-id="eda46-116">WebApp-Name</span><span class="sxs-lookup"><span data-stu-id="eda46-116">WebApp Name</span></span>

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

### <span data-ttu-id="eda46-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eda46-117">-ResourceGroupName</span></span>
<span data-ttu-id="eda46-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="eda46-118">Resource Group Name</span></span>

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

### <span data-ttu-id="eda46-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="eda46-119">-WebApp</span></span>
<span data-ttu-id="eda46-120">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="eda46-120">WebApp Object</span></span>

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

### <span data-ttu-id="eda46-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eda46-121">CommonParameters</span></span>
<span data-ttu-id="eda46-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eda46-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eda46-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eda46-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eda46-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eda46-124">INPUTS</span></span>

### <span data-ttu-id="eda46-125">System.String</span><span class="sxs-lookup"><span data-stu-id="eda46-125">System.String</span></span>

### <span data-ttu-id="eda46-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="eda46-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="eda46-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eda46-127">OUTPUTS</span></span>

### <span data-ttu-id="eda46-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span><span class="sxs-lookup"><span data-stu-id="eda46-128">Microsoft.Azure.Management.WebSites.Models.SlotConfigNamesResource</span></span>

## <span data-ttu-id="eda46-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="eda46-129">NOTES</span></span>

## <span data-ttu-id="eda46-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="eda46-130">RELATED LINKS</span></span>
