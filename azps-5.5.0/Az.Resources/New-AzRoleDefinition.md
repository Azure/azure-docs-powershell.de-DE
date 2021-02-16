---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150889"
---
# <span data-ttu-id="cb7b8-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cb7b8-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="cb7b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb7b8-102">SYNOPSIS</span></span>
<span data-ttu-id="cb7b8-103">Erstellt eine benutzerdefinierte Rolle in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="cb7b8-104">Geben Sie entweder eine JSON-Rollendefinitionsdatei oder ein "PSRoleDefinition"-Objekt als Eingabe an.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="cb7b8-105">Verwenden Sie zunächst den Befehl Get-AzRoleDefinition, um ein grundlegendes Rollendefinitionsobjekt zu generieren.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="cb7b8-106">Ändern Sie dann die Eigenschaften nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="cb7b8-107">Verwenden Sie zum Schluss diesen Befehl, um mithilfe der Rollendefinition eine benutzerdefinierte Rolle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="cb7b8-108">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb7b8-108">SYNTAX</span></span>

### <span data-ttu-id="cb7b8-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb7b8-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb7b8-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb7b8-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb7b8-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb7b8-111">DESCRIPTION</span></span>
<span data-ttu-id="cb7b8-112">Das New-AzRoleDefinition erstellt eine benutzerdefinierte Rolle in Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="cb7b8-113">Geben Sie eine Rollendefinition als Eingabe für den Befehl als Eine -JSON-Datei oder ein PSRoleDefinition-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="cb7b8-114">Die Definition der Eingaberolle MUSS die folgenden Eigenschaften enthalten:</span><span class="sxs-lookup"><span data-stu-id="cb7b8-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="cb7b8-115">DisplayName: der Name der benutzerdefinierten Rolle</span><span class="sxs-lookup"><span data-stu-id="cb7b8-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="cb7b8-116">Beschreibung: Eine kurze Beschreibung der Rolle, die den Zugriff zusammenfasst, den die Rolle gewährt.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="cb7b8-117">Aktionen: die Gruppe von Vorgängen, denen die benutzerdefinierte Rolle Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="cb7b8-118">Verwenden Get-AzProviderOperation, um den Vorgang für Azure-Ressourcenanbieter zu erhalten, die mit Azure RBAC gesichert werden können.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="cb7b8-119">Im Folgenden finden Sie einige gültige Vorgangszeichenfolgen:</span><span class="sxs-lookup"><span data-stu-id="cb7b8-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="cb7b8-120">"\*/read" gewährt Zugriff auf Lesevorgänge aller Azure-Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="cb7b8-121">"Microsoft.Network/\*/read" gewährt Zugriff auf Lesevorgänge für alle Ressourcentypen im Microsoft.Network-Ressourcenanbieter von Azure.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="cb7b8-122">"Microsoft.Compute/virtualMachines/\*" gewährt Zugriff auf alle Vorgänge virtueller Computer und deren untergeordnete Ressourcentypen.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="cb7b8-123">AssignableScopes: Die Gruppe von Bereiche (Azure-Abonnements oder Ressourcengruppen), in denen die benutzerdefinierte Rolle für die Zuweisung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="cb7b8-124">Mithilfe von "AssignableScopes" können Sie die benutzerdefinierte Rolle nur in den Abonnements oder Ressourcengruppen verfügbar machen, die sie benötigen, und die Benutzererfahrung für die restlichen Abonnements oder Ressourcengruppen nicht überladen.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="cb7b8-125">Im Folgenden finden Sie einige gültige zuzuordnende Bereiche:</span><span class="sxs-lookup"><span data-stu-id="cb7b8-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="cb7b8-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": macht die Rolle für Die Zuweisung in zwei Abonnements verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="cb7b8-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": macht die Rolle zur Zuweisung in einem einzigen Abonnement verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="cb7b8-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": macht die Rolle nur für Zuordnungen in der Netzwerkressourcengruppe verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="cb7b8-129">Die Definition der Eingaberolle kann die folgenden Eigenschaften enthalten:</span><span class="sxs-lookup"><span data-stu-id="cb7b8-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="cb7b8-130">NotActions: die Gruppe von Vorgängen, die von den Aktionen ausgeschlossen werden müssen, um die effektiven Aktionen für die benutzerdefinierte Rolle zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="cb7b8-131">Wenn es einen bestimmten Vorgang gibt, auf den Sie in einer benutzerdefinierten Rolle keinen Zugriff gewähren möchten, ist es praktisch, ihn mit NotActions auszuschließen, anstatt alle Anderen als diesen speziellen Vorgang in "Aktionen" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="cb7b8-132">DataActions: die Gruppe von Datenvorgängen, denen die benutzerdefinierte Rolle Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="cb7b8-133">NotDataActions: die Gruppe von Vorgängen, die von dataActions ausgeschlossen werden müssen, um die effektiven Datenaktionen für die benutzerdefinierte Rolle zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective data actions for the custom role.</span></span>
<span data-ttu-id="cb7b8-134">Wenn es einen bestimmten Datenvorgang gibt, auf den Sie in einer benutzerdefinierten Rolle keinen Zugriff gewähren möchten, ist es praktisch, notDataActions zu verwenden, um ihn auszuschließen, anstatt alle Anderen als diesen speziellen Vorgang in "Aktionen" anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="cb7b8-135">HINWEIS: Wenn einem Benutzer eine Rolle zugewiesen ist, die einen Vorgang in NotActions angibt, und außerdem einer anderen Rolle Zugriff auf denselben Vorgang gewährt wird, kann der Benutzer diesen Vorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="cb7b8-136">NotActions ist keine Verweigernregel, sondern einfach eine bequeme Möglichkeit, eine Reihe zulässiger Vorgänge zu erstellen, wenn bestimmte Vorgänge ausgeschlossen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="cb7b8-137">Es folgt eine json-Beispiel-Rollendefinition, die als Eingabe bereitgestellt werden kann { "Name": "Aktualisierte Rolle", "Beschreibung": "Kann alle Ressourcen überwachen und virtuelle Computer starten und neu starten", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action", \] "NotActions": \[ "*/write", \] "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs /read", \] "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write", \] "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="cb7b8-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="cb7b8-138">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cb7b8-138">EXAMPLES</span></span>

### <span data-ttu-id="cb7b8-139">Beispiel 1: Erstellen mit PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="cb7b8-139">Example 1: Create using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### <span data-ttu-id="cb7b8-140">Beispiel 2: Erstellen mit einer JSON-Datei</span><span class="sxs-lookup"><span data-stu-id="cb7b8-140">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="cb7b8-141">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb7b8-141">PARAMETERS</span></span>

### <span data-ttu-id="cb7b8-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb7b8-142">-DefaultProfile</span></span>
<span data-ttu-id="cb7b8-143">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cb7b8-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb7b8-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="cb7b8-144">-InputFile</span></span>
<span data-ttu-id="cb7b8-145">Dateiname, der eine einzelne json-Rollendefinition enthält.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-145">File name containing a single json role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb7b8-146">-Role</span><span class="sxs-lookup"><span data-stu-id="cb7b8-146">-Role</span></span>
<span data-ttu-id="cb7b8-147">Rollendefinitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-147">Role definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb7b8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb7b8-148">CommonParameters</span></span>
<span data-ttu-id="cb7b8-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb7b8-150">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb7b8-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb7b8-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cb7b8-151">INPUTS</span></span>

### <span data-ttu-id="cb7b8-152">Keine</span><span class="sxs-lookup"><span data-stu-id="cb7b8-152">None</span></span>

## <span data-ttu-id="cb7b8-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cb7b8-153">OUTPUTS</span></span>

### <span data-ttu-id="cb7b8-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cb7b8-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="cb7b8-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cb7b8-155">NOTES</span></span>
<span data-ttu-id="cb7b8-156">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="cb7b8-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="cb7b8-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cb7b8-157">RELATED LINKS</span></span>

[<span data-ttu-id="cb7b8-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="cb7b8-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="cb7b8-159">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cb7b8-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="cb7b8-160">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cb7b8-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="cb7b8-161">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cb7b8-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

