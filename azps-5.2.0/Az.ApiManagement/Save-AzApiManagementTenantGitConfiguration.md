---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3995506c302d2993623f12fcb7e6e2b9f96fd208
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300411"
---
# <span data-ttu-id="bfa59-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfa59-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="bfa59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfa59-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa59-103">Speichert Änderungen, indem ein Commit für die aktuelle Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bfa59-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="bfa59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfa59-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfa59-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bfa59-105">DESCRIPTION</span></span>
<span data-ttu-id="bfa59-106">Das **Cmdlet "Save-AzApiManagementTenantGitConfiguration"** speichert die Änderungen, indem ein Commit erstellt wird, der die aktuelle Konfigurationsmomentaufnahme für eine Verzweigung im Repository enthält.</span><span class="sxs-lookup"><span data-stu-id="bfa59-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="bfa59-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bfa59-107">EXAMPLES</span></span>

### <span data-ttu-id="bfa59-108">Beispiel 1: Speichern von Konfigurationsänderungen</span><span class="sxs-lookup"><span data-stu-id="bfa59-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="bfa59-109">Dieser Befehl speichert die Änderungen, indem ein Commit mit der aktuellen Konfigurationsmomentaufnahme für den angegebenen Zweig im Repository erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bfa59-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="bfa59-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfa59-110">PARAMETERS</span></span>

### <span data-ttu-id="bfa59-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="bfa59-111">-Branch</span></span>
<span data-ttu-id="bfa59-112">Gibt den Namen der Git-Verzweigung an, in der die aktuelle Konfigurationsmomentaufnahme festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfa59-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="bfa59-113">-Context</span><span class="sxs-lookup"><span data-stu-id="bfa59-113">-Context</span></span>
<span data-ttu-id="bfa59-114">Gibt ein **"PsApiManagementContext"-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="bfa59-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfa59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa59-115">-DefaultProfile</span></span>
<span data-ttu-id="bfa59-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bfa59-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfa59-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bfa59-117">-Force</span></span>
<span data-ttu-id="bfa59-118">Gibt an, dass dieses Cmdlet die aktuelle Konfigurationsdatenbank in das Git-Repository übernimmt, auch wenn das Git-Repository neuere Änderungen enthält, die überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bfa59-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="bfa59-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfa59-119">-PassThru</span></span>
<span data-ttu-id="bfa59-120">Gibt an, dass dieses Cmdlet ein **"PsApiManagementOperationResult"-Objekt** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="bfa59-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="bfa59-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfa59-121">-Confirm</span></span>
<span data-ttu-id="bfa59-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bfa59-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfa59-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="bfa59-123">-WhatIf</span></span>
<span data-ttu-id="bfa59-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bfa59-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfa59-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bfa59-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfa59-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa59-126">CommonParameters</span></span>
<span data-ttu-id="bfa59-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfa59-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa59-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfa59-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa59-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bfa59-129">INPUTS</span></span>

### <span data-ttu-id="bfa59-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bfa59-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bfa59-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bfa59-131">System.String</span></span>

### <span data-ttu-id="bfa59-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bfa59-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bfa59-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bfa59-133">OUTPUTS</span></span>

### <span data-ttu-id="bfa59-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="bfa59-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="bfa59-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bfa59-135">NOTES</span></span>

## <span data-ttu-id="bfa59-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bfa59-136">RELATED LINKS</span></span>

[<span data-ttu-id="bfa59-137">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="bfa59-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


