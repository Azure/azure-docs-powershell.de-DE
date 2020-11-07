---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 29be6682c18820a26966cd72997cf54f45db16f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824983"
---
# <span data-ttu-id="3c8c0-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3c8c0-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="3c8c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c8c0-102">SYNOPSIS</span></span>
<span data-ttu-id="3c8c0-103">Erstellt eine benutzerdefinierte Rolle in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="3c8c0-104">Stellen Sie entweder eine JSON-Rollen Definitionsdatei oder ein PSRoleDefinition-Objekt als eingabebereit.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="3c8c0-105">Verwenden Sie zuerst den Befehl Get-AzRoleDefinition, um ein Baseline-Rollen Definitionsobjekt zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="3c8c0-106">Ändern Sie dann die Eigenschaften nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="3c8c0-107">Verwenden Sie abschließend diesen Befehl, um eine benutzerdefinierte Rolle mithilfe der Rollendefinition zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="3c8c0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c8c0-108">SYNTAX</span></span>

### <span data-ttu-id="3c8c0-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c8c0-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c8c0-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c8c0-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c8c0-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c8c0-111">DESCRIPTION</span></span>
<span data-ttu-id="3c8c0-112">Das New-AzRoleDefinition-Cmdlet erstellt eine benutzerdefinierte Rolle in Azure Role-Based Zugriffssteuerung.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="3c8c0-113">Stellen Sie eine Rollendefinition als Eingabe für den Befehl als JSON-Datei oder als PSRoleDefinition-Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="3c8c0-114">Die Definition der Eingabe Rolle muss die folgenden Eigenschaften enthalten:</span><span class="sxs-lookup"><span data-stu-id="3c8c0-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="3c8c0-115">DisplayName: der Name der benutzerdefinierten Rolle</span><span class="sxs-lookup"><span data-stu-id="3c8c0-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="3c8c0-116">Beschreibung: eine kurze Beschreibung der Rolle, die den von der Rolle gewährten Zugriff zusammenfasst.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="3c8c0-117">Aktionen: die Gruppe von Vorgängen, denen die benutzerdefinierte Rolle Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="3c8c0-118">Verwenden Sie Get-AzProviderOperation, um den Vorgang für Azure-Ressourcenanbieter abzurufen, die mithilfe von Azure RBAC gesichert werden können.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="3c8c0-119">Im folgenden sind einige gültige Vorgangs Zeichenfolgen enthalten:</span><span class="sxs-lookup"><span data-stu-id="3c8c0-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="3c8c0-120">"\*/Read" gewährt Zugriff auf Lesevorgänge aller Azure-Ressourcenanbieter.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="3c8c0-121">"Microsoft. Network/\*/Read" gewährt Zugriff auf Lesevorgänge für alle Ressourcentypen im Microsoft. Network-Ressourcenanbieter von Azure.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="3c8c0-122">"Microsoft. Compute/virtualMachines/\*" gewährt Zugriff auf alle Vorgänge von virtuellen Computern und deren untergeordneten Ressourcentypen.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="3c8c0-123">AssignableScopes: die Gruppe von Bereichen (Azure-Abonnements oder Ressourcengruppen), in denen die benutzerdefinierte Rolle für die Zuweisung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="3c8c0-124">Mithilfe von AssignableScopes können Sie die benutzerdefinierte Rolle nur in den Abonnements oder Ressourcengruppen zur Verfügung stellen, die Sie benötigen, und nicht die Benutzeroberfläche für die restlichen Abonnements oder Ressourcengruppen überladen.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="3c8c0-125">Im folgenden finden Sie einige gültige beschreibbar-Bereiche:</span><span class="sxs-lookup"><span data-stu-id="3c8c0-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="3c8c0-126">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/Subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": stellt die Rolle in zwei Abonnements für die Zuweisung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="3c8c0-127">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": stellt die Rolle in einem einzigen Abonnement für die Zuweisung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="3c8c0-128">"/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": stellt die Rolle für die Zuweisung nur in der Netzwerkressourcen Gruppe zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="3c8c0-129">Die Definition der Eingabe Rolle kann die folgenden Eigenschaften enthalten:</span><span class="sxs-lookup"><span data-stu-id="3c8c0-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="3c8c0-130">Notacts: der Satz von Vorgängen, der aus den Aktionen ausgeschlossen werden muss, um die effektiven Aktionen für die benutzerdefinierte Rolle zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="3c8c0-131">Wenn es einen bestimmten Vorgang gibt, dem Sie in einer benutzerdefinierten Rolle keinen Zugriff gewähren möchten, empfiehlt es sich, ihn mithilfe von notacts auszuschließen, anstatt alle Vorgänge außer diesem bestimmten Vorgang in Aktionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="3c8c0-132">Daten Aktionen: die Gruppe von Datenvorgängen, denen die benutzerdefinierte Rolle Zugriff gewährt.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="3c8c0-133">NotDataActions: die Gruppe von Vorgängen, die aus den Daten Aktionen ausgeschlossen werden muss, um die effektiven Daten Aktionen für die benutzerdefinierte Rolle zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective data actions for the custom role.</span></span>
<span data-ttu-id="3c8c0-134">Wenn es einen bestimmten Datenvorgang gibt, dem Sie in einer benutzerdefinierten Rolle keinen Zugriff gewähren möchten, empfiehlt es sich, NotDataActions zu verwenden, um ihn auszuschließen, anstatt alle anderen Vorgänge als diesen bestimmten Vorgang in Aktionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="3c8c0-135">Hinweis: Wenn einem Benutzer eine Rolle zugewiesen wird, die einen Vorgang in notacts angibt und auch einer anderen Rolle zugewiesen wurde, wird der Zugriff auf denselben Vorgang gewährt – der Benutzer kann diesen Vorgang durchführen.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="3c8c0-136">Notacts ist keine Ablehnungsregel – es ist einfach eine bequeme Möglichkeit zum Erstellen einer Reihe von zulässigen Vorgängen, wenn bestimmte Vorgänge ausgeschlossen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="3c8c0-137">Im folgenden finden Sie eine JSON-Beispielrollen Definition, die als Eingabe {"Name": "aktualisierte Rolle", "Beschreibung": "kann alle Ressourcen überwachen und virtuelle Maschinen starten und neu starten", "Aktionen": \[ " */Read", "Microsoft. ClassicCompute/VirtualMachines/Restart/Aktion"; "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] ; "notacts": \[ "* /Write" \] ; "Daten Aktionen": \[ "Microsoft. Storage/storageAccounts/blobServices/Container/BLOBs/Read" \] ; "NotDataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/Container/BLOBs/Write" \] , "AssignableScopes": \[ "/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="3c8c0-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="3c8c0-138">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c8c0-138">EXAMPLES</span></span>

### <span data-ttu-id="3c8c0-139">Erstellen mithilfe von PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="3c8c0-139">Create using PSRoleDefinitionObject</span></span>
```
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

### <span data-ttu-id="3c8c0-140">Erstellen mit JSON-Datei</span><span class="sxs-lookup"><span data-stu-id="3c8c0-140">Create using JSON file</span></span>
```
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="3c8c0-141">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c8c0-141">PARAMETERS</span></span>

### <span data-ttu-id="3c8c0-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c8c0-142">-DefaultProfile</span></span>
<span data-ttu-id="3c8c0-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3c8c0-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c8c0-144">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="3c8c0-144">-InputFile</span></span>
<span data-ttu-id="3c8c0-145">Dateiname mit einer einzelnen JSON-Rollendefinition</span><span class="sxs-lookup"><span data-stu-id="3c8c0-145">File name containing a single json role definition.</span></span>

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

### <span data-ttu-id="3c8c0-146">-Role</span><span class="sxs-lookup"><span data-stu-id="3c8c0-146">-Role</span></span>
<span data-ttu-id="3c8c0-147">Rollen Definitionsobjekt</span><span class="sxs-lookup"><span data-stu-id="3c8c0-147">Role definition object.</span></span>

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

### <span data-ttu-id="3c8c0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c8c0-148">CommonParameters</span></span>
<span data-ttu-id="3c8c0-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c8c0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c8c0-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c8c0-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c8c0-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c8c0-151">INPUTS</span></span>

### <span data-ttu-id="3c8c0-152">Keine</span><span class="sxs-lookup"><span data-stu-id="3c8c0-152">None</span></span>

## <span data-ttu-id="3c8c0-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c8c0-153">OUTPUTS</span></span>

### <span data-ttu-id="3c8c0-154">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3c8c0-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="3c8c0-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c8c0-155">NOTES</span></span>
<span data-ttu-id="3c8c0-156">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="3c8c0-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="3c8c0-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c8c0-157">RELATED LINKS</span></span>

[<span data-ttu-id="3c8c0-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="3c8c0-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="3c8c0-159">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3c8c0-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="3c8c0-160">Satz-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3c8c0-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="3c8c0-161">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="3c8c0-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

