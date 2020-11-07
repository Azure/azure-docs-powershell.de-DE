---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: f0c22f199d19e97f957bc86fbee8d649d30b622d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664501"
---
# <span data-ttu-id="a9e89-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9e89-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="a9e89-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9e89-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e89-103">Ändert eine benutzerdefinierte Rolle in Azure RBAC.</span><span class="sxs-lookup"><span data-stu-id="a9e89-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="a9e89-104">Stellen Sie die geänderte Rollendefinition entweder als JSON-Datei oder als PSRoleDefinition bereit.</span><span class="sxs-lookup"><span data-stu-id="a9e89-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="a9e89-105">Verwenden Sie zuerst den Befehl Get-AzureRmRoleDefinition, um die benutzerdefinierte Rolle abzurufen, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="a9e89-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="a9e89-106">Ändern Sie dann die Eigenschaften, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="a9e89-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="a9e89-107">Speichern Sie die Rollendefinition schließlich mit diesem Befehl.</span><span class="sxs-lookup"><span data-stu-id="a9e89-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9e89-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9e89-108">SYNTAX</span></span>

### <span data-ttu-id="a9e89-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9e89-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9e89-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9e89-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9e89-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9e89-111">DESCRIPTION</span></span>
<span data-ttu-id="a9e89-112">Das Set-AzureRmRoleDefinition-Cmdlet aktualisiert eine vorhandene benutzerdefinierte Rolle in Azure Role-Based Zugriffssteuerung.</span><span class="sxs-lookup"><span data-stu-id="a9e89-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="a9e89-113">Stellen Sie die aktualisierte Rollendefinition als Eingabe für den Befehl als JSON-Datei oder als PSRoleDefinition-Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="a9e89-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="a9e89-114">Die Rollendefinition für die aktualisierte benutzerdefinierte Rolle muss die ID und alle anderen erforderlichen Eigenschaften der Rolle enthalten, auch wenn Sie nicht aktualisiert werden: DisplayName, Description, Actions, AssignableScopes.</span><span class="sxs-lookup"><span data-stu-id="a9e89-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="a9e89-115">Notacts, dataactions, NotDataActions sind optional.</span><span class="sxs-lookup"><span data-stu-id="a9e89-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="a9e89-116">Im folgenden finden Sie ein Beispiel für eine aktualisierte Rollendefinition JSON für Set-AzureRmRoleDefinition {"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "aktualisierte Rolle", "Beschreibung": "kann alle Ressourcen überwachen und virtuelle Computer starten und neu starten", "Aktionen": \[ " */Read", "Microsoft. ClassicCompute/VirtualMachines/Restart/Aktion"; "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] ; "notacts": \[ "* /Write" \] ; "Daten Aktionen": \[ "Microsoft. Storage/storageAccounts/blobServices/Container/BLOBs/Read" \] ; "NotDataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/Container/BLOBs/Write" \] , "AssignableScopes": \[ "/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="a9e89-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="a9e89-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9e89-117">EXAMPLES</span></span>

### <span data-ttu-id="a9e89-118">Aktualisieren mit PSRoleDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="a9e89-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="a9e89-119">Erstellen mit JSON-Datei</span><span class="sxs-lookup"><span data-stu-id="a9e89-119">Create using JSON file</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="a9e89-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9e89-120">PARAMETERS</span></span>

### <span data-ttu-id="a9e89-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e89-121">-DefaultProfile</span></span>
<span data-ttu-id="a9e89-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a9e89-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9e89-123">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="a9e89-123">-InputFile</span></span>
<span data-ttu-id="a9e89-124">Der Dateiname mit einer einzelnen JSON-Rollendefinition, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a9e89-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="a9e89-125">Schließen Sie nur die Eigenschaften ein, die in der JSON aktualisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9e89-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="a9e89-126">Die ID-Eigenschaft ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a9e89-126">Id property is Required.</span></span>

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

### <span data-ttu-id="a9e89-127">-Role</span><span class="sxs-lookup"><span data-stu-id="a9e89-127">-Role</span></span>
<span data-ttu-id="a9e89-128">Rollen Definitionsobjekt, das aktualisiert werden soll</span><span class="sxs-lookup"><span data-stu-id="a9e89-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="a9e89-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e89-129">CommonParameters</span></span>
<span data-ttu-id="a9e89-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9e89-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e89-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9e89-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e89-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9e89-132">INPUTS</span></span>

### <span data-ttu-id="a9e89-133">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9e89-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="a9e89-134">Parameter: role (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a9e89-134">Parameters: Role (ByValue)</span></span>

## <span data-ttu-id="a9e89-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9e89-135">OUTPUTS</span></span>

### <span data-ttu-id="a9e89-136">Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9e89-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="a9e89-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9e89-137">NOTES</span></span>
<span data-ttu-id="a9e89-138">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="a9e89-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a9e89-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9e89-139">RELATED LINKS</span></span>

[<span data-ttu-id="a9e89-140">Get-AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="a9e89-140">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="a9e89-141">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9e89-141">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="a9e89-142">Neu – AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9e89-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="a9e89-143">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="a9e89-143">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

