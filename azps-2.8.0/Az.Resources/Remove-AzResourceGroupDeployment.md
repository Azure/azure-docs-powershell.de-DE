---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: 2cae601904b15e2508886374c1b607ed8aec4b93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823404"
---
# <span data-ttu-id="26234-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26234-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="26234-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26234-102">SYNOPSIS</span></span>
<span data-ttu-id="26234-103">Entfernt eine Ressourcengruppen Bereitstellung und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="26234-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="26234-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26234-104">SYNTAX</span></span>

### <span data-ttu-id="26234-105">RemoveByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="26234-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26234-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="26234-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26234-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26234-107">DESCRIPTION</span></span>
<span data-ttu-id="26234-108">Das Cmdlet **Remove-AzResourceGroupDeployment** entfernt eine Azure Resource Group-Bereitstellung und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="26234-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="26234-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26234-109">EXAMPLES</span></span>

## <span data-ttu-id="26234-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="26234-110">PARAMETERS</span></span>

### <span data-ttu-id="26234-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="26234-111">-ApiVersion</span></span>
<span data-ttu-id="26234-112">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="26234-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="26234-113">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="26234-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="26234-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26234-114">-DefaultProfile</span></span>
<span data-ttu-id="26234-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="26234-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26234-116">-ID</span><span class="sxs-lookup"><span data-stu-id="26234-116">-Id</span></span>
<span data-ttu-id="26234-117">Gibt die ID der zu entfernenden Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="26234-117">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26234-118">-Name</span><span class="sxs-lookup"><span data-stu-id="26234-118">-Name</span></span>
<span data-ttu-id="26234-119">Gibt den Namen der zu entfernenden Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="26234-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26234-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="26234-120">-Pre</span></span>
<span data-ttu-id="26234-121">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="26234-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="26234-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26234-122">-ResourceGroupName</span></span>
<span data-ttu-id="26234-123">Gibt den Namen der zu entfernenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="26234-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26234-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="26234-124">-Confirm</span></span>
<span data-ttu-id="26234-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26234-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26234-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26234-126">-WhatIf</span></span>
<span data-ttu-id="26234-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26234-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26234-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26234-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26234-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26234-129">CommonParameters</span></span>
<span data-ttu-id="26234-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26234-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26234-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26234-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26234-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26234-132">INPUTS</span></span>

### <span data-ttu-id="26234-133">System. String</span><span class="sxs-lookup"><span data-stu-id="26234-133">System.String</span></span>

## <span data-ttu-id="26234-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26234-134">OUTPUTS</span></span>

### <span data-ttu-id="26234-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26234-135">System.Boolean</span></span>

## <span data-ttu-id="26234-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="26234-136">NOTES</span></span>

## <span data-ttu-id="26234-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26234-137">RELATED LINKS</span></span>

[<span data-ttu-id="26234-138">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26234-138">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="26234-139">Neu – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26234-139">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="26234-140">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26234-140">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="26234-141">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="26234-141">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


