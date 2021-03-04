---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: eb865535fcb4ee49b834e923fcf3f319ff5de074
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925376"
---
# <span data-ttu-id="a430a-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="a430a-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="a430a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a430a-102">SYNOPSIS</span></span>
<span data-ttu-id="a430a-103">Speichert Änderungen, indem ein Commit für die aktuelle Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a430a-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="a430a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a430a-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a430a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a430a-105">DESCRIPTION</span></span>
<span data-ttu-id="a430a-106">Das **Cmdlet Save-AzApiManagementTenantGitConfiguration** speichert die Änderungen, indem ein Commit erstellt wird, der die aktuelle Konfigurationsmomentaufnahme in einer Verzweigung im Repository enthält.</span><span class="sxs-lookup"><span data-stu-id="a430a-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="a430a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a430a-107">EXAMPLES</span></span>

### <span data-ttu-id="a430a-108">Beispiel 1: Speichern von Änderungen an der Konfiguration</span><span class="sxs-lookup"><span data-stu-id="a430a-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="a430a-109">Mit diesem Befehl werden die Änderungen gespeichert, indem ein Commit mit der aktuellen Konfigurationsmomentaufnahme für die angegebene Verzweigung im Repository erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a430a-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="a430a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a430a-110">PARAMETERS</span></span>

### <span data-ttu-id="a430a-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="a430a-111">-Branch</span></span>
<span data-ttu-id="a430a-112">Gibt den Namen der Git-Verzweigung an, in der die aktuelle Konfigurationsmomentaufnahme festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a430a-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="a430a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a430a-113">-Context</span></span>
<span data-ttu-id="a430a-114">Gibt ein **PsApiManagementContext-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="a430a-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a430a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a430a-115">-DefaultProfile</span></span>
<span data-ttu-id="a430a-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a430a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a430a-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="a430a-117">-Force</span></span>
<span data-ttu-id="a430a-118">Gibt an, dass dieses Cmdlet die aktuelle Konfigurationsdatenbank an das Git-Repository übergibt, auch wenn das Git-Repository neuere Änderungen enthält, die überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a430a-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="a430a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a430a-119">-PassThru</span></span>
<span data-ttu-id="a430a-120">Gibt an, dass dieses Cmdlet ein **PsApiManagementOperationResult-Objekt** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a430a-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="a430a-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a430a-121">-Confirm</span></span>
<span data-ttu-id="a430a-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a430a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a430a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a430a-123">-WhatIf</span></span>
<span data-ttu-id="a430a-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a430a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a430a-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a430a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a430a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a430a-126">CommonParameters</span></span>
<span data-ttu-id="a430a-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a430a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a430a-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a430a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a430a-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a430a-129">INPUTS</span></span>

### <span data-ttu-id="a430a-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a430a-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a430a-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a430a-131">System.String</span></span>

### <span data-ttu-id="a430a-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a430a-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a430a-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a430a-133">OUTPUTS</span></span>

### <span data-ttu-id="a430a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="a430a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="a430a-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a430a-135">NOTES</span></span>

## <span data-ttu-id="a430a-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a430a-136">RELATED LINKS</span></span>

[<span data-ttu-id="a430a-137">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="a430a-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


