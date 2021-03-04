---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 7c443625294b3a23ac79dfcbabb724a2d3fceaa3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928488"
---
# <span data-ttu-id="4967e-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="4967e-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="4967e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4967e-102">SYNOPSIS</span></span>
<span data-ttu-id="4967e-103">Sicherheitseinstellungen in Azure Security Center erhalten</span><span class="sxs-lookup"><span data-stu-id="4967e-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="4967e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4967e-104">SYNTAX</span></span>

### <span data-ttu-id="4967e-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="4967e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4967e-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4967e-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4967e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4967e-107">DESCRIPTION</span></span>
<span data-ttu-id="4967e-108">Das Get-AzSecuritySetting cmdlet erhalten Sicherheitseinstellungen in Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="4967e-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="4967e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4967e-109">EXAMPLES</span></span>

### <span data-ttu-id="4967e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4967e-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="4967e-111">Ruft eine EINSTELLUNG für den MCAS-Datenexport ab.</span><span class="sxs-lookup"><span data-stu-id="4967e-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="4967e-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4967e-112">PARAMETERS</span></span>

### <span data-ttu-id="4967e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4967e-113">-DefaultProfile</span></span>
<span data-ttu-id="4967e-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4967e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4967e-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="4967e-115">-SettingName</span></span>
<span data-ttu-id="4967e-116">Einstellungsname.</span><span class="sxs-lookup"><span data-stu-id="4967e-116">Setting name.</span></span> <span data-ttu-id="4967e-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="4967e-117">(MCAS/WDATP)</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4967e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4967e-118">CommonParameters</span></span>
<span data-ttu-id="4967e-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4967e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4967e-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4967e-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4967e-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4967e-121">INPUTS</span></span>

### <span data-ttu-id="4967e-122">System.String</span><span class="sxs-lookup"><span data-stu-id="4967e-122">System.String</span></span>

## <span data-ttu-id="4967e-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4967e-123">OUTPUTS</span></span>

### <span data-ttu-id="4967e-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="4967e-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="4967e-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="4967e-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="4967e-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4967e-126">NOTES</span></span>

## <span data-ttu-id="4967e-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4967e-127">RELATED LINKS</span></span>
