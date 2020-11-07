---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: da66d0cacbddbeb53972308faa681bde42c813d2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843231"
---
# <span data-ttu-id="e1ca3-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e1ca3-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="e1ca3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1ca3-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ca3-103">Entfernt eine Ressourcengruppen Bereitstellung und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e1ca3-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="e1ca3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1ca3-104">SYNTAX</span></span>

### <span data-ttu-id="e1ca3-105">RemoveByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1ca3-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1ca3-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="e1ca3-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1ca3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1ca3-107">DESCRIPTION</span></span>
<span data-ttu-id="e1ca3-108">Das Cmdlet **Remove-AzResourceGroupDeployment** entfernt eine Azure Resource Group-Bereitstellung und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="e1ca3-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="e1ca3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1ca3-109">EXAMPLES</span></span>

## <span data-ttu-id="e1ca3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1ca3-110">PARAMETERS</span></span>

### <span data-ttu-id="e1ca3-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e1ca3-111">-ApiVersion</span></span>
<span data-ttu-id="e1ca3-112">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e1ca3-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e1ca3-113">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="e1ca3-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e1ca3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ca3-114">-DefaultProfile</span></span>
<span data-ttu-id="e1ca3-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e1ca3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1ca3-116">-ID</span><span class="sxs-lookup"><span data-stu-id="e1ca3-116">-Id</span></span>
<span data-ttu-id="e1ca3-117">Gibt die ID der zu entfernenden Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="e1ca3-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="e1ca3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e1ca3-118">-Name</span></span>
<span data-ttu-id="e1ca3-119">Gibt den Namen der zu entfernenden Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="e1ca3-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ca3-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="e1ca3-120">-Pre</span></span>
<span data-ttu-id="e1ca3-121">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e1ca3-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e1ca3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ca3-122">-ResourceGroupName</span></span>
<span data-ttu-id="e1ca3-123">Gibt den Namen der zu entfernenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e1ca3-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ca3-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1ca3-124">-Confirm</span></span>
<span data-ttu-id="e1ca3-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1ca3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1ca3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1ca3-126">-WhatIf</span></span>
<span data-ttu-id="e1ca3-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1ca3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1ca3-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1ca3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1ca3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ca3-129">CommonParameters</span></span>
<span data-ttu-id="e1ca3-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ca3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ca3-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ca3-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ca3-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1ca3-132">INPUTS</span></span>

### <span data-ttu-id="e1ca3-133">Keine</span><span class="sxs-lookup"><span data-stu-id="e1ca3-133">None</span></span>

## <span data-ttu-id="e1ca3-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1ca3-134">OUTPUTS</span></span>

## <span data-ttu-id="e1ca3-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1ca3-135">NOTES</span></span>

## <span data-ttu-id="e1ca3-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1ca3-136">RELATED LINKS</span></span>

[<span data-ttu-id="e1ca3-137">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e1ca3-137">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="e1ca3-138">Neu – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e1ca3-138">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="e1ca3-139">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e1ca3-139">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="e1ca3-140">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="e1ca3-140">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


