---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 4a2293384cdf2cf579458d05c112469d096bfd9a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470292"
---
# <span data-ttu-id="bcc41-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="bcc41-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="bcc41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcc41-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc41-103">Bereitstellung eines Azure AD-Administrators für Synapse Analytics SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="bcc41-103">Provisions an Azure AD administrator for Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="bcc41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcc41-104">SYNTAX</span></span>

### <span data-ttu-id="bcc41-105">SetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bcc41-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcc41-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcc41-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcc41-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcc41-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcc41-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bcc41-108">DESCRIPTION</span></span>
<span data-ttu-id="bcc41-109">Das **Cmdlet "Set-AzSynapseSqlActiveDirectoryAdministrator"** stellt einen Azure Active Directory (Azure AD)-Administrator für Azure Synapse Analytics Workspace im aktuellen Abonnement bereit.</span><span class="sxs-lookup"><span data-stu-id="bcc41-109">The **Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace in the current subscription.</span></span>
<span data-ttu-id="bcc41-110">Sie können immer nur einen Administrator gleichzeitig bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="bcc41-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="bcc41-111">Die folgenden Mitglieder von Azure AD können als Synapse Analytics Workspace-Administrator bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="bcc41-111">The following members of Azure AD can be provisioned as a Synapse Analytics Workspace administrator:</span></span>
- <span data-ttu-id="bcc41-112">Native Mitglieder von Azure AD</span><span class="sxs-lookup"><span data-stu-id="bcc41-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="bcc41-113">Verbundmitglieder von Azure AD</span><span class="sxs-lookup"><span data-stu-id="bcc41-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="bcc41-114">Importierte Mitglieder aus anderen Azure ADs, die native Mitglieder oder Partnermitglieder sind</span><span class="sxs-lookup"><span data-stu-id="bcc41-114">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="bcc41-115">Azure AD-Gruppen, die als Sicherheitsgruppen für Microsoft-Konten erstellt wurden, z. B. in den Domänen Outlook.com, Hotmail.com oder Live.com, werden als Administratoren nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bcc41-115">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="bcc41-116">Andere Gastkonten, z. B. in den Gmail.com oder Yahoo.com, werden als Administratoren nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bcc41-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="bcc41-117">Es wird empfohlen, eine dedizierte Azure AD-Gruppe als Administrator bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="bcc41-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="bcc41-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bcc41-118">EXAMPLES</span></span>

### <span data-ttu-id="bcc41-119">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bcc41-119">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

<span data-ttu-id="bcc41-120">Mit diesem Befehl wird eine Azure AD-Administratorgruppe namens DBAs für den Arbeitsbereich "ContosoWorkspace" bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="bcc41-120">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="bcc41-121">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bcc41-121">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

<span data-ttu-id="bcc41-122">Mit diesem Befehl wird eine Azure AD-Administratorgruppe namens DBAs für den Arbeitsbereich "ContosoWorkspace" bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="bcc41-122">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="bcc41-123">Dadurch wird sichergestellt, dass der Befehl auch dann erfolgreich ist, wenn der Anzeigename der Gruppe nicht eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="bcc41-123">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="bcc41-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcc41-124">PARAMETERS</span></span>

### <span data-ttu-id="bcc41-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcc41-125">-AsJob</span></span>
<span data-ttu-id="bcc41-126">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bcc41-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bcc41-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc41-127">-DefaultProfile</span></span>
<span data-ttu-id="bcc41-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bcc41-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcc41-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bcc41-129">-DisplayName</span></span>
<span data-ttu-id="bcc41-130">Gibt den Anzeigenamen des Benutzers oder der Gruppe an, dem bzw. der Berechtigungen erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="bcc41-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="bcc41-131">Dieser Anzeigename muss in dem Active Directory vorhanden sein, das dem aktuellen Abonnement zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bcc41-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="bcc41-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcc41-132">-InputObject</span></span>
<span data-ttu-id="bcc41-133">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="bcc41-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc41-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bcc41-134">-ObjectId</span></span>
<span data-ttu-id="bcc41-135">Gibt die Objekt-ID des Benutzers oder der Gruppe in Azure Active Directory an, für den Berechtigungen erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="bcc41-135">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc41-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcc41-136">-ResourceGroupName</span></span>
<span data-ttu-id="bcc41-137">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="bcc41-137">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc41-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcc41-138">-ResourceId</span></span>
<span data-ttu-id="bcc41-139">Ressourcenbezeichner des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="bcc41-139">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc41-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bcc41-140">-WorkspaceName</span></span>
<span data-ttu-id="bcc41-141">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="bcc41-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc41-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcc41-142">-Confirm</span></span>
<span data-ttu-id="bcc41-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bcc41-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcc41-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bcc41-144">-WhatIf</span></span>
<span data-ttu-id="bcc41-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bcc41-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcc41-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bcc41-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcc41-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc41-147">CommonParameters</span></span>
<span data-ttu-id="bcc41-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcc41-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc41-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcc41-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc41-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bcc41-150">INPUTS</span></span>

### <span data-ttu-id="bcc41-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bcc41-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="bcc41-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bcc41-152">OUTPUTS</span></span>

### <span data-ttu-id="bcc41-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="bcc41-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="bcc41-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bcc41-154">NOTES</span></span>

## <span data-ttu-id="bcc41-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bcc41-155">RELATED LINKS</span></span>
