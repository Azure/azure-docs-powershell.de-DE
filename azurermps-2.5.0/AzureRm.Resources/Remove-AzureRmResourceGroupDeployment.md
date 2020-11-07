---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroupdeployment
schema: 2.0.0
ms.openlocfilehash: bfe0bad0104708e635b49f02cfb1eecd2474ea5b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850536"
---
# <span data-ttu-id="dbb48-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dbb48-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="dbb48-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbb48-102">SYNOPSIS</span></span>
<span data-ttu-id="dbb48-103">Entfernt eine Ressourcengruppen Bereitstellung und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="dbb48-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbb48-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbb48-104">SYNTAX</span></span>

### <span data-ttu-id="dbb48-105">RemoveByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbb48-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbb48-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="dbb48-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbb48-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbb48-107">DESCRIPTION</span></span>
<span data-ttu-id="dbb48-108">Das Cmdlet **Remove-AzureRmResourceGroupDeployment** entfernt eine Azure Resource Group-Bereitstellung und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="dbb48-108">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="dbb48-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbb48-109">EXAMPLES</span></span>

## <span data-ttu-id="dbb48-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbb48-110">PARAMETERS</span></span>

### <span data-ttu-id="dbb48-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dbb48-111">-ApiVersion</span></span>
<span data-ttu-id="dbb48-112">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="dbb48-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="dbb48-113">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="dbb48-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="dbb48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbb48-114">-DefaultProfile</span></span>
<span data-ttu-id="dbb48-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dbb48-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbb48-116">-ID</span><span class="sxs-lookup"><span data-stu-id="dbb48-116">-Id</span></span>
<span data-ttu-id="dbb48-117">Gibt die ID der zu entfernenden Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="dbb48-117">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="dbb48-118">-Name</span><span class="sxs-lookup"><span data-stu-id="dbb48-118">-Name</span></span>
<span data-ttu-id="dbb48-119">Gibt den Namen der zu entfernenden Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="dbb48-119">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="dbb48-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="dbb48-120">-Pre</span></span>
<span data-ttu-id="dbb48-121">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="dbb48-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="dbb48-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbb48-122">-ResourceGroupName</span></span>
<span data-ttu-id="dbb48-123">Gibt den Namen der zu entfernenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="dbb48-123">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="dbb48-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dbb48-124">-Confirm</span></span>
<span data-ttu-id="dbb48-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbb48-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbb48-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbb48-126">-WhatIf</span></span>
<span data-ttu-id="dbb48-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbb48-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbb48-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbb48-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbb48-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbb48-129">CommonParameters</span></span>
<span data-ttu-id="dbb48-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbb48-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbb48-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbb48-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbb48-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbb48-132">INPUTS</span></span>

### <span data-ttu-id="dbb48-133">Keine</span><span class="sxs-lookup"><span data-stu-id="dbb48-133">None</span></span>

## <span data-ttu-id="dbb48-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbb48-134">OUTPUTS</span></span>

## <span data-ttu-id="dbb48-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbb48-135">NOTES</span></span>

## <span data-ttu-id="dbb48-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbb48-136">RELATED LINKS</span></span>

[<span data-ttu-id="dbb48-137">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dbb48-137">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="dbb48-138">Neu – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dbb48-138">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="dbb48-139">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dbb48-139">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="dbb48-140">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="dbb48-140">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


