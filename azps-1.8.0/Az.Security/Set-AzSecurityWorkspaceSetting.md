---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 679b1458b3e749b2ccfca3863f745edd562ffc2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659427"
---
# <span data-ttu-id="9e4ca-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="9e4ca-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="9e4ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e4ca-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4ca-103">Aktualisiert die Arbeitsbereichseinstellungen für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e4ca-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="9e4ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e4ca-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e4ca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e4ca-105">DESCRIPTION</span></span>
<span data-ttu-id="9e4ca-106">Aktualisiert die Arbeitsbereichseinstellungen für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e4ca-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="9e4ca-107">Der konfigurierte Arbeitsbereich enthält die Sicherheitsdaten, die vom Sicherheitsagenten erfasst wurden, der in VMs innerhalb dieses Abonnements installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9e4ca-107">The configured workspace will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="9e4ca-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e4ca-108">EXAMPLES</span></span>

### <span data-ttu-id="9e4ca-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9e4ca-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="9e4ca-110">Legt den Arbeitsbereich "Mein Arbeitsbereich" so fest, dass alle Sicherheitsdaten enthalten sind, die von den Sicherheits-Agents erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="9e4ca-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the security agents.</span></span>

## <span data-ttu-id="9e4ca-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e4ca-111">PARAMETERS</span></span>

### <span data-ttu-id="9e4ca-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4ca-112">-DefaultProfile</span></span>
<span data-ttu-id="9e4ca-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e4ca-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e4ca-114">-Name</span><span class="sxs-lookup"><span data-stu-id="9e4ca-114">-Name</span></span>
<span data-ttu-id="9e4ca-115">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="9e4ca-115">Resource name.</span></span>

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

### <span data-ttu-id="9e4ca-116">-Scope</span><span class="sxs-lookup"><span data-stu-id="9e4ca-116">-Scope</span></span>
<span data-ttu-id="9e4ca-117">Bereich.</span><span class="sxs-lookup"><span data-stu-id="9e4ca-117">Scope.</span></span>

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

### <span data-ttu-id="9e4ca-118">-Arbeitsbereichs-Nr</span><span class="sxs-lookup"><span data-stu-id="9e4ca-118">-WorkspaceId</span></span>
<span data-ttu-id="9e4ca-119">Arbeitsbereichs-ID.</span><span class="sxs-lookup"><span data-stu-id="9e4ca-119">Workspace ID.</span></span>

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

### <span data-ttu-id="9e4ca-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9e4ca-120">-Confirm</span></span>
<span data-ttu-id="9e4ca-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e4ca-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e4ca-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e4ca-122">-WhatIf</span></span>
<span data-ttu-id="9e4ca-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e4ca-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e4ca-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e4ca-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e4ca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4ca-125">CommonParameters</span></span>
<span data-ttu-id="9e4ca-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e4ca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4ca-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e4ca-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4ca-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e4ca-128">INPUTS</span></span>

### <span data-ttu-id="9e4ca-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9e4ca-129">System.String</span></span>

## <span data-ttu-id="9e4ca-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e4ca-130">OUTPUTS</span></span>

### <span data-ttu-id="9e4ca-131">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="9e4ca-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="9e4ca-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e4ca-132">NOTES</span></span>

## <span data-ttu-id="9e4ca-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e4ca-133">RELATED LINKS</span></span>
