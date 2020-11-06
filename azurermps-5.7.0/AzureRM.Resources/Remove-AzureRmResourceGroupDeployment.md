---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: ce1d614050f9b70bfe4ed2ff4d242f1a6f38c55f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498841"
---
# <span data-ttu-id="2504f-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2504f-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="2504f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2504f-102">SYNOPSIS</span></span>
<span data-ttu-id="2504f-103">Entfernt eine Ressourcengruppen Bereitstellung und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="2504f-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2504f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2504f-104">SYNTAX</span></span>

### <span data-ttu-id="2504f-105">RemoveByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2504f-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2504f-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="2504f-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2504f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2504f-107">DESCRIPTION</span></span>
<span data-ttu-id="2504f-108">Das Cmdlet **Remove-AzureRmResourceGroupDeployment** entfernt eine Azure Resource Group-Bereitstellung und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="2504f-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="2504f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2504f-109">EXAMPLES</span></span>

## <span data-ttu-id="2504f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2504f-110">PARAMETERS</span></span>

### <span data-ttu-id="2504f-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2504f-111">-ApiVersion</span></span>
<span data-ttu-id="2504f-112">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2504f-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2504f-113">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="2504f-113">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2504f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2504f-114">-DefaultProfile</span></span>
<span data-ttu-id="2504f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2504f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2504f-116">-ID</span><span class="sxs-lookup"><span data-stu-id="2504f-116">-Id</span></span>
<span data-ttu-id="2504f-117">Gibt die ID der zu entfernenden Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="2504f-117">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2504f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2504f-118">-Name</span></span>
<span data-ttu-id="2504f-119">Gibt den Namen der zu entfernenden Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="2504f-119">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2504f-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="2504f-120">-Pre</span></span>
<span data-ttu-id="2504f-121">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2504f-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2504f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2504f-122">-ResourceGroupName</span></span>
<span data-ttu-id="2504f-123">Gibt den Namen der zu entfernenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2504f-123">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2504f-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2504f-124">-Confirm</span></span>
<span data-ttu-id="2504f-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2504f-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2504f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2504f-126">-WhatIf</span></span>
<span data-ttu-id="2504f-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2504f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2504f-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2504f-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2504f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2504f-129">CommonParameters</span></span>
<span data-ttu-id="2504f-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2504f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2504f-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2504f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2504f-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2504f-132">INPUTS</span></span>

### <span data-ttu-id="2504f-133">Keine</span><span class="sxs-lookup"><span data-stu-id="2504f-133">None</span></span>
<span data-ttu-id="2504f-134">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2504f-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2504f-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2504f-135">OUTPUTS</span></span>

### <span data-ttu-id="2504f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2504f-136">System.Boolean</span></span>

## <span data-ttu-id="2504f-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="2504f-137">NOTES</span></span>

## <span data-ttu-id="2504f-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2504f-138">RELATED LINKS</span></span>

[<span data-ttu-id="2504f-139">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2504f-139">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2504f-140">Neu – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2504f-140">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2504f-141">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2504f-141">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2504f-142">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2504f-142">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


