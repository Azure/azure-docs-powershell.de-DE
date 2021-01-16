---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 288bb02ffad3669615df3535aec7f691162daa2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291383"
---
# <span data-ttu-id="74c68-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="74c68-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="74c68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74c68-102">SYNOPSIS</span></span>
<span data-ttu-id="74c68-103">Veröffentlicht Änderungen aus einer Git-Verzweigung in der Konfigurationsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="74c68-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="74c68-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74c68-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74c68-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74c68-105">DESCRIPTION</span></span>
<span data-ttu-id="74c68-106">Das **Cmdlet Publish-AzApiManagementTenantGitConfiguration** veröffentlicht die Änderungen von einer Git-Verzweigung in die Konfigurationsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="74c68-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="74c68-107">Alternativ können Sie die Änderungen in einer Git-Verzweigung überprüfen, ohne sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="74c68-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="74c68-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74c68-108">EXAMPLES</span></span>

### <span data-ttu-id="74c68-109">Beispiel 1: Bereitstellen von Git-Änderungen</span><span class="sxs-lookup"><span data-stu-id="74c68-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="74c68-110">Mit diesem Befehl werden die Änderungen aus der angegebenen Verzweigung in der Konfigurationsdatenbank veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="74c68-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="74c68-111">Beispiel 2: Überprüfen von Git-Änderungen</span><span class="sxs-lookup"><span data-stu-id="74c68-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="74c68-112">Mit diesem Befehl werden die Änderungen in der Git-Verzweigung anhand der Konfigurationsdatenbank überprüft.</span><span class="sxs-lookup"><span data-stu-id="74c68-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="74c68-113">Änderungen werden nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="74c68-113">It does not publish changes.</span></span>

## <span data-ttu-id="74c68-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74c68-114">PARAMETERS</span></span>

### <span data-ttu-id="74c68-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="74c68-115">-Branch</span></span>
<span data-ttu-id="74c68-116">Gibt den Namen der Git-Verzweigung an, über die dieses Cmdlet die Konfiguration in der Konfigurationsdatenbank implementiert.</span><span class="sxs-lookup"><span data-stu-id="74c68-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c68-117">-Context</span><span class="sxs-lookup"><span data-stu-id="74c68-117">-Context</span></span>
<span data-ttu-id="74c68-118">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="74c68-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c68-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74c68-119">-DefaultProfile</span></span>
<span data-ttu-id="74c68-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74c68-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74c68-121">-Force</span><span class="sxs-lookup"><span data-stu-id="74c68-121">-Force</span></span>
<span data-ttu-id="74c68-122">Zeigt an, dass mit diesem Cmdlet Abonnements für Produkte gelöscht werden, die in diesem Update gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="74c68-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c68-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74c68-123">-PassThru</span></span>
<span data-ttu-id="74c68-124">Gibt an, dass dieses Cmdlet ein **"PsApiManagementOperationResult"-Objekt** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="74c68-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c68-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="74c68-125">-ValidateOnly</span></span>
<span data-ttu-id="74c68-126">Gibt an, dass dieses Cmdlet die Änderungen in der angegebenen Git-Verzweigung überprüft.</span><span class="sxs-lookup"><span data-stu-id="74c68-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="74c68-127">Es wird nicht in der Konfigurationsdatenbank veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="74c68-127">It does not publish to the configuration database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74c68-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74c68-128">-Confirm</span></span>
<span data-ttu-id="74c68-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74c68-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74c68-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="74c68-130">-WhatIf</span></span>
<span data-ttu-id="74c68-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74c68-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74c68-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74c68-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74c68-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74c68-133">CommonParameters</span></span>
<span data-ttu-id="74c68-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74c68-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74c68-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74c68-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74c68-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74c68-136">INPUTS</span></span>

### <span data-ttu-id="74c68-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="74c68-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="74c68-138">System.String</span><span class="sxs-lookup"><span data-stu-id="74c68-138">System.String</span></span>

### <span data-ttu-id="74c68-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="74c68-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="74c68-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74c68-140">OUTPUTS</span></span>

### <span data-ttu-id="74c68-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="74c68-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="74c68-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="74c68-142">NOTES</span></span>

## <span data-ttu-id="74c68-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="74c68-143">RELATED LINKS</span></span>

[<span data-ttu-id="74c68-144">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="74c68-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


