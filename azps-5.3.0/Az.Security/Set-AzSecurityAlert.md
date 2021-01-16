---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 0555b86b6e5240adfc43bc52153bf14d7612be1b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382541"
---
# <span data-ttu-id="ecfbe-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="ecfbe-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="ecfbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecfbe-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfbe-103">Aktualisiert einen Sicherheitswarnungszustand.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-103">Updates a security alert state.</span></span>

## <span data-ttu-id="ecfbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecfbe-104">SYNTAX</span></span>

### <span data-ttu-id="ecfbe-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="ecfbe-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfbe-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="ecfbe-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfbe-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecfbe-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecfbe-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="ecfbe-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecfbe-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ecfbe-109">DESCRIPTION</span></span>
<span data-ttu-id="ecfbe-110">Legt einen Sicherheitswarnungszustand fest.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-110">Sets a security alert state.</span></span>

## <span data-ttu-id="ecfbe-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ecfbe-111">EXAMPLES</span></span>

### <span data-ttu-id="ecfbe-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ecfbe-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="ecfbe-113">Schließt eine ausgelöste Sicherheitswarnung.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="ecfbe-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecfbe-114">PARAMETERS</span></span>

### <span data-ttu-id="ecfbe-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="ecfbe-115">-ActionType</span></span>
<span data-ttu-id="ecfbe-116">Aktionstyp.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-116">Action Type.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfbe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecfbe-117">-DefaultProfile</span></span>
<span data-ttu-id="ecfbe-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecfbe-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecfbe-119">-InputObject</span></span>
<span data-ttu-id="ecfbe-120">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfbe-121">-Location</span><span class="sxs-lookup"><span data-stu-id="ecfbe-121">-Location</span></span>
<span data-ttu-id="ecfbe-122">"Ort" aus.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-122">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfbe-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ecfbe-123">-Name</span></span>
<span data-ttu-id="ecfbe-124">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfbe-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecfbe-125">-PassThru</span></span>
<span data-ttu-id="ecfbe-126">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="ecfbe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecfbe-127">-ResourceGroupName</span></span>
<span data-ttu-id="ecfbe-128">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecfbe-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecfbe-129">-ResourceId</span></span>
<span data-ttu-id="ecfbe-130">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-130">Resource ID.</span></span>

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

### <span data-ttu-id="ecfbe-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecfbe-131">-Confirm</span></span>
<span data-ttu-id="ecfbe-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecfbe-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ecfbe-133">-WhatIf</span></span>
<span data-ttu-id="ecfbe-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecfbe-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecfbe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfbe-136">CommonParameters</span></span>
<span data-ttu-id="ecfbe-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfbe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfbe-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ecfbe-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfbe-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ecfbe-139">INPUTS</span></span>

### <span data-ttu-id="ecfbe-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ecfbe-140">System.String</span></span>

### <span data-ttu-id="ecfbe-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="ecfbe-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="ecfbe-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ecfbe-142">OUTPUTS</span></span>

### <span data-ttu-id="ecfbe-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ecfbe-143">System.Boolean</span></span>

## <span data-ttu-id="ecfbe-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ecfbe-144">NOTES</span></span>

## <span data-ttu-id="ecfbe-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ecfbe-145">RELATED LINKS</span></span>
