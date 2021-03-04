---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 6bcee25399004d5fb8f485e9c58446713bedc5c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945736"
---
# <span data-ttu-id="b6e0a-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="b6e0a-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="b6e0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6e0a-102">SYNOPSIS</span></span>
<span data-ttu-id="b6e0a-103">Aktualisiert die Arbeitsbereichseinstellungen für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6e0a-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="b6e0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6e0a-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6e0a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6e0a-105">DESCRIPTION</span></span>
<span data-ttu-id="b6e0a-106">Aktualisiert die Arbeitsbereichseinstellungen für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6e0a-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="b6e0a-107">Der konfigurierte Arbeitsbereich enthält die Sicherheitsdaten, die vom Azure Log Analytics-Agent gesammelt wurden, der in VMs innerhalb dieses Abonnements installiert ist.</span><span class="sxs-lookup"><span data-stu-id="b6e0a-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="b6e0a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b6e0a-108">EXAMPLES</span></span>

### <span data-ttu-id="b6e0a-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b6e0a-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="b6e0a-110">Legt den Arbeitsbereich "securityuserws" so fest, dass alle Vom Azure Log Analytics-Agent gesammelten Sicherheitsdaten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b6e0a-110">Sets the "securityuserws" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="b6e0a-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b6e0a-111">PARAMETERS</span></span>

### <span data-ttu-id="b6e0a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6e0a-112">-DefaultProfile</span></span>
<span data-ttu-id="b6e0a-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6e0a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6e0a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="b6e0a-114">-Name</span></span>
<span data-ttu-id="b6e0a-115">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="b6e0a-115">Resource name.</span></span>

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

### <span data-ttu-id="b6e0a-116">-Scope</span><span class="sxs-lookup"><span data-stu-id="b6e0a-116">-Scope</span></span>
<span data-ttu-id="b6e0a-117">Bereich.</span><span class="sxs-lookup"><span data-stu-id="b6e0a-117">Scope.</span></span>

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

### <span data-ttu-id="b6e0a-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="b6e0a-118">-WorkspaceId</span></span>
<span data-ttu-id="b6e0a-119">Arbeitsbereichs-ID.</span><span class="sxs-lookup"><span data-stu-id="b6e0a-119">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6e0a-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b6e0a-120">-Confirm</span></span>
<span data-ttu-id="b6e0a-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b6e0a-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e0a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6e0a-122">-WhatIf</span></span>
<span data-ttu-id="b6e0a-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6e0a-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6e0a-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6e0a-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6e0a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6e0a-125">CommonParameters</span></span>
<span data-ttu-id="b6e0a-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6e0a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6e0a-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6e0a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6e0a-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b6e0a-128">INPUTS</span></span>

### <span data-ttu-id="b6e0a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b6e0a-129">System.String</span></span>

## <span data-ttu-id="b6e0a-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b6e0a-130">OUTPUTS</span></span>

### <span data-ttu-id="b6e0a-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="b6e0a-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="b6e0a-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b6e0a-132">NOTES</span></span>

## <span data-ttu-id="b6e0a-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b6e0a-133">RELATED LINKS</span></span>
