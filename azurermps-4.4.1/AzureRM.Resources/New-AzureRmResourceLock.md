---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6847ECFD-2E3D-46F6-ABE9-9D8E08C7858F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResourceLock.md
ms.openlocfilehash: c363279c0cbb6dc20b0ddcc7bae32266a848fb3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504750"
---
# <span data-ttu-id="b6635-101">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="b6635-101">New-AzureRmResourceLock</span></span>

## <span data-ttu-id="b6635-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6635-102">SYNOPSIS</span></span>
<span data-ttu-id="b6635-103">Erstellt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="b6635-103">Creates a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6635-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6635-104">SYNTAX</span></span>

### <span data-ttu-id="b6635-105">Eine Sperre im angegebenen Bereich.</span><span class="sxs-lookup"><span data-stu-id="b6635-105">A lock at the specified scope.</span></span> <span data-ttu-id="b6635-106">Standard</span><span class="sxs-lookup"><span data-stu-id="b6635-106">(Default)</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -Scope <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6635-107">Eine Sperre im Bereich der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b6635-107">A lock at the resource group scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6635-108">Eine Sperre für den Ressourcengruppen-Ressourcenbereich.</span><span class="sxs-lookup"><span data-stu-id="b6635-108">A lock at the resource group resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6635-109">Eine Sperre im Abonnement Bereich.</span><span class="sxs-lookup"><span data-stu-id="b6635-109">A lock at the subscription scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6635-110">Eine Sperre für den Ressourcenbereich des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="b6635-110">A lock at the subscription resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6635-111">Eine Sperre im Mandanten Ressourcenbereich.</span><span class="sxs-lookup"><span data-stu-id="b6635-111">A lock at the tenant resource scope.</span></span>
```
New-AzureRmResourceLock -LockName <String> -LockLevel <LockLevel> [-LockNotes <String>] [-Force]
 -ResourceName <String> -ResourceType <String> [-TenantLevel] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6635-112">Eine Sperre, nach ID.</span><span class="sxs-lookup"><span data-stu-id="b6635-112">A lock, by Id.</span></span>
```
New-AzureRmResourceLock -LockLevel <LockLevel> [-LockNotes <String>] [-Force] -LockId <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6635-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6635-113">DESCRIPTION</span></span>
<span data-ttu-id="b6635-114">Das Cmdlet **New-AzureRmResourceLock** erstellt eine Ressourcensperre.</span><span class="sxs-lookup"><span data-stu-id="b6635-114">The **New-AzureRmResourceLock** cmdlet creates a resource lock.</span></span>

## <span data-ttu-id="b6635-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6635-115">EXAMPLES</span></span>

### <span data-ttu-id="b6635-116">Beispiel 1: Erstellen einer Ressourcensperre auf einer Website</span><span class="sxs-lookup"><span data-stu-id="b6635-116">Example 1: Create a resource lock on a website</span></span>
```
PS C:\>New-AzureRmResourceLock -LockLevel CanNotDelete -LockNotes "My lock notes" -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites"
```

<span data-ttu-id="b6635-117">Dieser Befehl erstellt eine Ressourcensperre auf einer Website.</span><span class="sxs-lookup"><span data-stu-id="b6635-117">This command creates a resource lock on a website.</span></span>

## <span data-ttu-id="b6635-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6635-118">PARAMETERS</span></span>

### <span data-ttu-id="b6635-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b6635-119">-ApiVersion</span></span>
<span data-ttu-id="b6635-120">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="b6635-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b6635-121">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="b6635-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b6635-122">-Force</span></span>
<span data-ttu-id="b6635-123">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="b6635-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6635-124">-Information</span><span class="sxs-lookup"><span data-stu-id="b6635-124">-InformationAction</span></span>
<span data-ttu-id="b6635-125">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="b6635-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b6635-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b6635-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6635-127">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="b6635-127">Continue</span></span>
- <span data-ttu-id="b6635-128">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="b6635-128">Ignore</span></span>
- <span data-ttu-id="b6635-129">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="b6635-129">Inquire</span></span>
- <span data-ttu-id="b6635-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b6635-130">SilentlyContinue</span></span>
- <span data-ttu-id="b6635-131">Beenden</span><span class="sxs-lookup"><span data-stu-id="b6635-131">Stop</span></span>
- <span data-ttu-id="b6635-132">Anhalten</span><span class="sxs-lookup"><span data-stu-id="b6635-132">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b6635-133">-InformationVariable</span></span>
<span data-ttu-id="b6635-134">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="b6635-134">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-135">-Sperre</span><span class="sxs-lookup"><span data-stu-id="b6635-135">-LockId</span></span>
<span data-ttu-id="b6635-136">Gibt die ID der Sperre an.</span><span class="sxs-lookup"><span data-stu-id="b6635-136">Specifies the ID of the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-137">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="b6635-137">-LockLevel</span></span>
<span data-ttu-id="b6635-138">Gibt die Ebene für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="b6635-138">Specifies the level for the lock.</span></span>
<span data-ttu-id="b6635-139">Derzeit ist der einzige gültige Wert können.</span><span class="sxs-lookup"><span data-stu-id="b6635-139">Currently, the only valid value is CanNotDelete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Locks.LockLevel
Parameter Sets: (All)
Aliases: Level

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-140">-LockName</span><span class="sxs-lookup"><span data-stu-id="b6635-140">-LockName</span></span>
<span data-ttu-id="b6635-141">Gibt den Namen der Sperre an.</span><span class="sxs-lookup"><span data-stu-id="b6635-141">Specifies the name of the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope., A lock at the resource group scope., A lock at the resource group resource scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-142">-Sie LockNotes</span><span class="sxs-lookup"><span data-stu-id="b6635-142">-LockNotes</span></span>
<span data-ttu-id="b6635-143">Gibt die Notizen für die Sperre an.</span><span class="sxs-lookup"><span data-stu-id="b6635-143">Specifies the notes for the lock.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Notes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="b6635-144">-Pre</span></span>
<span data-ttu-id="b6635-145">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b6635-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b6635-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6635-146">-ResourceGroupName</span></span>
<span data-ttu-id="b6635-147">Gibt den Namen einer Ressourcengruppe an, für die die Sperre gilt oder die die Ressourcengruppe enthält, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="b6635-147">Specifies the name of a resource group for which the lock applies or that contains the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b6635-148">-ResourceName</span></span>
<span data-ttu-id="b6635-149">Gibt den Namen der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="b6635-149">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="b6635-150">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="b6635-150">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-151">-</span><span class="sxs-lookup"><span data-stu-id="b6635-151">-ResourceType</span></span>
<span data-ttu-id="b6635-152">Gibt den Ressourcentyp der Ressource an, für die die Sperre gilt.</span><span class="sxs-lookup"><span data-stu-id="b6635-152">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-153">-Scope</span><span class="sxs-lookup"><span data-stu-id="b6635-153">-Scope</span></span>
<span data-ttu-id="b6635-154">Gibt den Bereich an, auf den die Sperre angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b6635-154">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="b6635-155">Wenn Sie beispielsweise eine Datenbank angeben möchten, verwenden Sie das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="b6635-155">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="b6635-156">`/subscriptions/`Abonnement-ID- `/resourceGroups/` Ressourcengruppenname `/providers/Microsoft.Sql/servers/` Servername der Datenbankname `/databases/`</span><span class="sxs-lookup"><span data-stu-id="b6635-156">`/subscriptions/`subscription ID`/resourceGroups/`resource group name`/providers/Microsoft.Sql/servers/`server name`/databases/`database name</span></span>

<span data-ttu-id="b6635-157">Verwenden Sie das folgende Format, um eine Ressourcengruppe anzugeben:</span><span class="sxs-lookup"><span data-stu-id="b6635-157">To specify a resource group, use the following format:</span></span> 

<span data-ttu-id="b6635-158">`/subscriptions/`Name der Ressourcengruppe der Abonnement-ID `/resourceGroups/`</span><span class="sxs-lookup"><span data-stu-id="b6635-158">`/subscriptions/`subscription ID`/resourceGroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="b6635-159">-TenantLevel</span></span>
<span data-ttu-id="b6635-160">Gibt an, dass dieses Cmdlet auf Mandantenebene funktioniert.</span><span class="sxs-lookup"><span data-stu-id="b6635-160">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-161">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b6635-161">-Confirm</span></span>
<span data-ttu-id="b6635-162">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b6635-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6635-163">-WhatIf</span></span>
<span data-ttu-id="b6635-164">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6635-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6635-165">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6635-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6635-166">-DefaultProfile</span></span>
<span data-ttu-id="b6635-167">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6635-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6635-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6635-168">CommonParameters</span></span>
<span data-ttu-id="b6635-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6635-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6635-170">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6635-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6635-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6635-171">INPUTS</span></span>

## <span data-ttu-id="b6635-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6635-172">OUTPUTS</span></span>

### <span data-ttu-id="b6635-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="b6635-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b6635-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6635-174">NOTES</span></span>

## <span data-ttu-id="b6635-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6635-175">RELATED LINKS</span></span>

[<span data-ttu-id="b6635-176">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="b6635-176">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="b6635-177">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="b6635-177">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="b6635-178">Satz-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="b6635-178">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


