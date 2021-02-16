---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: a02d2685987844db5f88fafaf12d0c9aed4a3234
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169020"
---
# <span data-ttu-id="d649b-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="d649b-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="d649b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d649b-102">SYNOPSIS</span></span>
<span data-ttu-id="d649b-103">Aktualisiert die Arbeitsbereichseinstellungen für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d649b-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="d649b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d649b-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d649b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d649b-105">DESCRIPTION</span></span>
<span data-ttu-id="d649b-106">Aktualisiert die Arbeitsbereichseinstellungen für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d649b-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="d649b-107">Der konfigurierte Arbeitsbereich enthält die Sicherheitsdaten, die vom Azure Log Analytics-Agent gesammelt wurden, der in VMs innerhalb dieses Abonnements in VMs installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d649b-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="d649b-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d649b-108">EXAMPLES</span></span>

### <span data-ttu-id="d649b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d649b-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="d649b-110">Legt den Arbeitsbereich "securityuserws" so fest, dass er alle Sicherheitsdaten enthält, die vom Azure Log Analytics-Agent gesammelt wurden.</span><span class="sxs-lookup"><span data-stu-id="d649b-110">Sets the "securityuserws" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="d649b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d649b-111">PARAMETERS</span></span>

### <span data-ttu-id="d649b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d649b-112">-DefaultProfile</span></span>
<span data-ttu-id="d649b-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d649b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d649b-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d649b-114">-Name</span></span>
<span data-ttu-id="d649b-115">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d649b-115">Resource name.</span></span>

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

### <span data-ttu-id="d649b-116">-Scope</span><span class="sxs-lookup"><span data-stu-id="d649b-116">-Scope</span></span>
<span data-ttu-id="d649b-117">Bereich.</span><span class="sxs-lookup"><span data-stu-id="d649b-117">Scope.</span></span>

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

### <span data-ttu-id="d649b-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="d649b-118">-WorkspaceId</span></span>
<span data-ttu-id="d649b-119">Arbeitsbereichs-ID.</span><span class="sxs-lookup"><span data-stu-id="d649b-119">Workspace ID.</span></span>

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

### <span data-ttu-id="d649b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d649b-120">-Confirm</span></span>
<span data-ttu-id="d649b-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d649b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d649b-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d649b-122">-WhatIf</span></span>
<span data-ttu-id="d649b-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d649b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d649b-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d649b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d649b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d649b-125">CommonParameters</span></span>
<span data-ttu-id="d649b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d649b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d649b-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d649b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d649b-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d649b-128">INPUTS</span></span>

### <span data-ttu-id="d649b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d649b-129">System.String</span></span>

## <span data-ttu-id="d649b-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d649b-130">OUTPUTS</span></span>

### <span data-ttu-id="d649b-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="d649b-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="d649b-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d649b-132">NOTES</span></span>

## <span data-ttu-id="d649b-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d649b-133">RELATED LINKS</span></span>
