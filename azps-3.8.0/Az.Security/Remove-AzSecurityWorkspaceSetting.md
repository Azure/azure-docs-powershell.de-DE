---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 79780c101296d78115a1c88ef4d4aebcd3721c22
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996285"
---
# <span data-ttu-id="e5e5e-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="e5e5e-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="e5e5e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e5e-103">Löscht die Einstellungen für den Sicherheits Arbeitsbereich für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="e5e5e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5e5e-104">SYNTAX</span></span>

### <span data-ttu-id="e5e5e-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="e5e5e-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5e5e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5e5e-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5e5e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e5e5e-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5e5e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5e5e-108">DESCRIPTION</span></span>
<span data-ttu-id="e5e5e-109">Löscht die Einstellungen für den Sicherheits Arbeitsbereich für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="e5e5e-110">Mit dieser Aktion werden die neu installierten Sicherheits-Agents an den Standardarbeitsbereich dieses Abonnements gemeldet.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="e5e5e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5e5e-111">EXAMPLES</span></span>

### <span data-ttu-id="e5e5e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5e5e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="e5e5e-113">Löscht die Einstellungen für den Sicherheits Arbeitsbereich für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="e5e5e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5e5e-114">PARAMETERS</span></span>

### <span data-ttu-id="e5e5e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e5e-115">-DefaultProfile</span></span>
<span data-ttu-id="e5e5e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5e5e-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e5e5e-117">-InputObject</span></span>
<span data-ttu-id="e5e5e-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e5e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e5e5e-119">-Name</span></span>
<span data-ttu-id="e5e5e-120">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="e5e5e-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e5e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5e5e-121">-PassThru</span></span>
<span data-ttu-id="e5e5e-122">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-122">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e5e-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e5e5e-123">-ResourceId</span></span>
<span data-ttu-id="e5e5e-124">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-124">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5e5e-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5e5e-125">-Confirm</span></span>
<span data-ttu-id="e5e5e-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5e5e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5e5e-127">-WhatIf</span></span>
<span data-ttu-id="e5e5e-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5e5e-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5e5e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e5e-130">CommonParameters</span></span>
<span data-ttu-id="e5e5e-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5e5e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e5e-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e5e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e5e-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5e5e-133">INPUTS</span></span>

### <span data-ttu-id="e5e5e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e5e5e-134">System.String</span></span>

### <span data-ttu-id="e5e5e-135">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="e5e5e-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="e5e5e-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5e5e-136">OUTPUTS</span></span>

### <span data-ttu-id="e5e5e-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e5e5e-137">System.Boolean</span></span>

## <span data-ttu-id="e5e5e-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5e5e-138">NOTES</span></span>

## <span data-ttu-id="e5e5e-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5e5e-139">RELATED LINKS</span></span>
