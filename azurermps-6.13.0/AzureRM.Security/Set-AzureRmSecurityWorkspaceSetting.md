---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 3d2fdd8b6a1763aea97da3967fb2696857e7fd75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499414"
---
# <span data-ttu-id="81f98-101">Set-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="81f98-101">Set-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="81f98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81f98-102">SYNOPSIS</span></span>
<span data-ttu-id="81f98-103">Aktualisiert die Arbeitsbereichseinstellungen für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81f98-103">Updates the workspace settings for the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81f98-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81f98-104">SYNTAX</span></span>

```
Set-AzureRmSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81f98-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81f98-105">DESCRIPTION</span></span>
<span data-ttu-id="81f98-106">Aktualisiert die Arbeitsbereichseinstellungen für das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81f98-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="81f98-107">Der konfigurierte Arbeitsbereich enthält die Sicherheitsdaten, die vom Sicherheitsagenten erfasst wurden, der in VMs innerhalb dieses Abonnements installiert ist.</span><span class="sxs-lookup"><span data-stu-id="81f98-107">The configured workspace will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="81f98-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81f98-108">EXAMPLES</span></span>

### <span data-ttu-id="81f98-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81f98-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="81f98-110">Legt den Arbeitsbereich "Mein Arbeitsbereich" so fest, dass alle Sicherheitsdaten enthalten sind, die von den Sicherheits-Agents erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="81f98-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the security agents.</span></span>

## <span data-ttu-id="81f98-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="81f98-111">PARAMETERS</span></span>

### <span data-ttu-id="81f98-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f98-112">-DefaultProfile</span></span>
<span data-ttu-id="81f98-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81f98-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81f98-114">-Name</span><span class="sxs-lookup"><span data-stu-id="81f98-114">-Name</span></span>
<span data-ttu-id="81f98-115">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="81f98-115">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81f98-116">-Scope</span><span class="sxs-lookup"><span data-stu-id="81f98-116">-Scope</span></span>
<span data-ttu-id="81f98-117">Bereich.</span><span class="sxs-lookup"><span data-stu-id="81f98-117">Scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81f98-118">-Arbeitsbereichs-Nr</span><span class="sxs-lookup"><span data-stu-id="81f98-118">-WorkspaceId</span></span>
<span data-ttu-id="81f98-119">Arbeitsbereichs-ID.</span><span class="sxs-lookup"><span data-stu-id="81f98-119">Workspace ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81f98-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="81f98-120">-Confirm</span></span>
<span data-ttu-id="81f98-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="81f98-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81f98-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81f98-122">-WhatIf</span></span>
<span data-ttu-id="81f98-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81f98-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="81f98-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="81f98-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81f98-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f98-125">CommonParameters</span></span>
<span data-ttu-id="81f98-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81f98-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f98-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81f98-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f98-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81f98-128">INPUTS</span></span>

### <span data-ttu-id="81f98-129">System. String</span><span class="sxs-lookup"><span data-stu-id="81f98-129">System.String</span></span>

## <span data-ttu-id="81f98-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81f98-130">OUTPUTS</span></span>

### <span data-ttu-id="81f98-131">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="81f98-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="81f98-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="81f98-132">NOTES</span></span>

## <span data-ttu-id="81f98-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81f98-133">RELATED LINKS</span></span>
