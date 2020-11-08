---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 75e68cfac55c8fb7086f02d5e70dc466f335d1de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178216"
---
# <span data-ttu-id="854df-101">Remove-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="854df-101">Remove-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="854df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="854df-102">SYNOPSIS</span></span>
<span data-ttu-id="854df-103">Löscht die Einstellungen für den Sicherheits Arbeitsbereich für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="854df-103">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="854df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="854df-104">SYNTAX</span></span>

### <span data-ttu-id="854df-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="854df-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="854df-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="854df-106">ResourceId</span></span>
```
Remove-AzSecurityWorkspaceSetting -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="854df-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="854df-107">InputObject</span></span>
```
Remove-AzSecurityWorkspaceSetting -InputObject <PSSecurityWorkspaceSetting> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="854df-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="854df-108">DESCRIPTION</span></span>
<span data-ttu-id="854df-109">Löscht die Einstellungen für den Sicherheits Arbeitsbereich für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="854df-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="854df-110">Mit dieser Aktion werden die neu installierten Sicherheits-Agents an den Standardarbeitsbereich dieses Abonnements gemeldet.</span><span class="sxs-lookup"><span data-stu-id="854df-110">This action will make the newly installed security agents to report to the default workspace of this subscription.</span></span>

## <span data-ttu-id="854df-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="854df-111">EXAMPLES</span></span>

### <span data-ttu-id="854df-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="854df-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="854df-113">Löscht die Einstellungen für den Sicherheits Arbeitsbereich für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="854df-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="854df-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="854df-114">PARAMETERS</span></span>

### <span data-ttu-id="854df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="854df-115">-DefaultProfile</span></span>
<span data-ttu-id="854df-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="854df-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="854df-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="854df-117">-InputObject</span></span>
<span data-ttu-id="854df-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="854df-118">Input Object.</span></span>

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

### <span data-ttu-id="854df-119">-Name</span><span class="sxs-lookup"><span data-stu-id="854df-119">-Name</span></span>
<span data-ttu-id="854df-120">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="854df-120">Resource name.</span></span>

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

### <span data-ttu-id="854df-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="854df-121">-PassThru</span></span>
<span data-ttu-id="854df-122">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="854df-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="854df-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="854df-123">-ResourceId</span></span>
<span data-ttu-id="854df-124">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="854df-124">Resource ID.</span></span>

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

### <span data-ttu-id="854df-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="854df-125">-Confirm</span></span>
<span data-ttu-id="854df-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="854df-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="854df-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="854df-127">-WhatIf</span></span>
<span data-ttu-id="854df-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="854df-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="854df-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="854df-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="854df-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="854df-130">CommonParameters</span></span>
<span data-ttu-id="854df-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="854df-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="854df-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="854df-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="854df-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="854df-133">INPUTS</span></span>

### <span data-ttu-id="854df-134">System. String</span><span class="sxs-lookup"><span data-stu-id="854df-134">System.String</span></span>

### <span data-ttu-id="854df-135">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="854df-135">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="854df-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="854df-136">OUTPUTS</span></span>

### <span data-ttu-id="854df-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="854df-137">System.Boolean</span></span>

## <span data-ttu-id="854df-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="854df-138">NOTES</span></span>

## <span data-ttu-id="854df-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="854df-139">RELATED LINKS</span></span>
