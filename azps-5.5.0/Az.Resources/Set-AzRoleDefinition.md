---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: c68ad7def1b94796a020ffd29495e2b4c0b15a60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150857"
---
# <span data-ttu-id="cb95f-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cb95f-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="cb95f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb95f-102">SYNOPSIS</span></span>
<span data-ttu-id="cb95f-103">Ändert eine benutzerdefinierte Rolle in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="cb95f-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="cb95f-104">Geben Sie die geänderte Rollendefinition entweder als Eine -JSON-Datei oder als PSRoleDefinition an.</span><span class="sxs-lookup"><span data-stu-id="cb95f-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="cb95f-105">Verwenden Sie zunächst den Befehl Get-AzRoleDefinition, um die benutzerdefinierte Rolle abzurufen, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="cb95f-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="cb95f-106">Ändern Sie dann die Eigenschaften, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="cb95f-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="cb95f-107">Speichern Sie schließlich die Rollendefinition mit diesem Befehl.</span><span class="sxs-lookup"><span data-stu-id="cb95f-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="cb95f-108">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cb95f-108">SYNTAX</span></span>

### <span data-ttu-id="cb95f-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb95f-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb95f-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb95f-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb95f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb95f-111">DESCRIPTION</span></span>
<span data-ttu-id="cb95f-112">Das Set-AzRoleDefinition aktualisiert eine vorhandene benutzerdefinierte Rolle in Azure Role-Based Access Control.</span><span class="sxs-lookup"><span data-stu-id="cb95f-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="cb95f-113">Geben Sie die aktualisierte Rollendefinition als Eingabe für den Befehl als Eine -JSON-Datei oder ein PSRoleDefinition-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="cb95f-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="cb95f-114">Die Rollendefinition für die aktualisierte benutzerdefinierte Rolle MUSS die ID und alle anderen erforderlichen Eigenschaften der Rolle enthalten, auch wenn sie nicht aktualisiert werden: "DisplayName", "Description", "Actions", "AssignableScopes".</span><span class="sxs-lookup"><span data-stu-id="cb95f-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="cb95f-115">NotActions, DataActions, NotDataActions sind optional.</span><span class="sxs-lookup"><span data-stu-id="cb95f-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="cb95f-116">Es folgt ein Beispiel mit aktualisierter Rollendefinition für Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Aktualisierte Rolle", "Beschreibung": "Kann alle Ressourcen überwachen und virtuelle Computer starten und neu starten", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action", \] "NotActions": \[ "*/write", \] "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read", \] "NotDataActions": \[ "Microsoft.Storage/storageAccount \] "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="cb95f-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="cb95f-117">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cb95f-117">EXAMPLES</span></span>

### <span data-ttu-id="cb95f-118">Beispiel 1: Aktualisieren mit PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="cb95f-118">Example 1: Update using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="cb95f-119">Beispiel 2: Erstellen mit einer JSON-Datei</span><span class="sxs-lookup"><span data-stu-id="cb95f-119">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="cb95f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb95f-120">PARAMETERS</span></span>

### <span data-ttu-id="cb95f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb95f-121">-DefaultProfile</span></span>
<span data-ttu-id="cb95f-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cb95f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb95f-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="cb95f-123">-InputFile</span></span>
<span data-ttu-id="cb95f-124">Dateiname, der eine einzelne json-Rollendefinition enthält, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb95f-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="cb95f-125">Schließen Sie nur die Eigenschaften ein, die im JSON aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cb95f-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="cb95f-126">Die Eigenschaft "ID" ist "Required".</span><span class="sxs-lookup"><span data-stu-id="cb95f-126">Id property is Required.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb95f-127">-Role</span><span class="sxs-lookup"><span data-stu-id="cb95f-127">-Role</span></span>
<span data-ttu-id="cb95f-128">Zu aktualisierende Rollendefinitionsobjekt</span><span class="sxs-lookup"><span data-stu-id="cb95f-128">Role definition object to be updated</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb95f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb95f-129">CommonParameters</span></span>
<span data-ttu-id="cb95f-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb95f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb95f-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb95f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb95f-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cb95f-132">INPUTS</span></span>

### <span data-ttu-id="cb95f-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cb95f-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="cb95f-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cb95f-134">OUTPUTS</span></span>

### <span data-ttu-id="cb95f-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cb95f-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="cb95f-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cb95f-136">NOTES</span></span>
<span data-ttu-id="cb95f-137">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span><span class="sxs-lookup"><span data-stu-id="cb95f-137">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="cb95f-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cb95f-138">RELATED LINKS</span></span>

[<span data-ttu-id="cb95f-139">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="cb95f-139">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="cb95f-140">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cb95f-140">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="cb95f-141">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cb95f-141">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="cb95f-142">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="cb95f-142">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

