---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176083"
---
# <span data-ttu-id="8a5c4-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="8a5c4-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="8a5c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a5c4-102">SYNOPSIS</span></span>
<span data-ttu-id="8a5c4-103">Abrufen von Sicherheitseinstellungen im Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="8a5c4-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="8a5c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a5c4-104">SYNTAX</span></span>

### <span data-ttu-id="8a5c4-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a5c4-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a5c4-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="8a5c4-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a5c4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a5c4-107">DESCRIPTION</span></span>
<span data-ttu-id="8a5c4-108">Das Get-AzSecuritySetting-Cmdlet erhalten Sicherheitseinstellungen im Azure Security Center.</span><span class="sxs-lookup"><span data-stu-id="8a5c4-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="8a5c4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a5c4-109">EXAMPLES</span></span>

### <span data-ttu-id="8a5c4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a5c4-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="8a5c4-111">Ruft eine MCAS-Datenexport Einstellung ab</span><span class="sxs-lookup"><span data-stu-id="8a5c4-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="8a5c4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a5c4-112">PARAMETERS</span></span>

### <span data-ttu-id="8a5c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a5c4-113">-DefaultProfile</span></span>
<span data-ttu-id="8a5c4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a5c4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a5c4-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="8a5c4-115">-SettingName</span></span>
<span data-ttu-id="8a5c4-116">Name der Einstellung.</span><span class="sxs-lookup"><span data-stu-id="8a5c4-116">Setting name.</span></span> <span data-ttu-id="8a5c4-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="8a5c4-117">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="8a5c4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a5c4-118">CommonParameters</span></span>
<span data-ttu-id="8a5c4-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a5c4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a5c4-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a5c4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a5c4-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a5c4-121">INPUTS</span></span>

### <span data-ttu-id="8a5c4-122">System. String</span><span class="sxs-lookup"><span data-stu-id="8a5c4-122">System.String</span></span>

## <span data-ttu-id="8a5c4-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a5c4-123">OUTPUTS</span></span>

### <span data-ttu-id="8a5c4-124">Microsoft. Azure. Commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="8a5c4-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="8a5c4-125">Microsoft. Azure. Commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="8a5c4-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="8a5c4-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a5c4-126">NOTES</span></span>

## <span data-ttu-id="8a5c4-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a5c4-127">RELATED LINKS</span></span>
