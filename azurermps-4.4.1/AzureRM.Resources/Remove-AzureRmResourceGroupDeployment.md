---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 84aa6f50d02f4c85de674c163565a205f2b83750
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500713"
---
# <span data-ttu-id="39103-101">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="39103-101">Remove-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="39103-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39103-102">SYNOPSIS</span></span>
<span data-ttu-id="39103-103">Entfernt eine Ressourcengruppen Bereitstellung und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="39103-103">Removes a resource group deployment and any associated operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39103-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39103-104">SYNTAX</span></span>

### <span data-ttu-id="39103-105">Der Parametersatz für den Bereitstellungsnamen.</span><span class="sxs-lookup"><span data-stu-id="39103-105">The deployment name parameter set.</span></span> <span data-ttu-id="39103-106">Standard</span><span class="sxs-lookup"><span data-stu-id="39103-106">(Default)</span></span>
```
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <String> -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39103-107">Der Parametersatz für die Bereitstellungs-ID.</span><span class="sxs-lookup"><span data-stu-id="39103-107">The deployment Id parameter set.</span></span>
```
Remove-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39103-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39103-108">DESCRIPTION</span></span>
<span data-ttu-id="39103-109">Das Cmdlet **Remove-AzureRmResourceGroupDeployment** entfernt eine Azure Resource Group-Bereitstellung und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="39103-109">The **Remove-AzureRmResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="39103-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39103-110">EXAMPLES</span></span>

## <span data-ttu-id="39103-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="39103-111">PARAMETERS</span></span>

### <span data-ttu-id="39103-112">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="39103-112">-ApiVersion</span></span>
<span data-ttu-id="39103-113">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="39103-113">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="39103-114">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="39103-114">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="39103-115">-ID</span><span class="sxs-lookup"><span data-stu-id="39103-115">-Id</span></span>
<span data-ttu-id="39103-116">Gibt die ID der zu entfernenden Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="39103-116">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39103-117">-Name</span><span class="sxs-lookup"><span data-stu-id="39103-117">-Name</span></span>
<span data-ttu-id="39103-118">Gibt den Namen der zu entfernenden Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="39103-118">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39103-119">-Pre</span><span class="sxs-lookup"><span data-stu-id="39103-119">-Pre</span></span>
<span data-ttu-id="39103-120">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="39103-120">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="39103-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39103-121">-ResourceGroupName</span></span>
<span data-ttu-id="39103-122">Gibt den Namen der zu entfernenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="39103-122">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39103-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39103-123">-Confirm</span></span>
<span data-ttu-id="39103-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39103-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39103-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39103-125">-WhatIf</span></span>
<span data-ttu-id="39103-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39103-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39103-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39103-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39103-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39103-128">-DefaultProfile</span></span>
<span data-ttu-id="39103-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39103-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39103-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39103-130">CommonParameters</span></span>
<span data-ttu-id="39103-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39103-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39103-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39103-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39103-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39103-133">INPUTS</span></span>

## <span data-ttu-id="39103-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39103-134">OUTPUTS</span></span>

### <span data-ttu-id="39103-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39103-135">System.Boolean</span></span>

## <span data-ttu-id="39103-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="39103-136">NOTES</span></span>

## <span data-ttu-id="39103-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39103-137">RELATED LINKS</span></span>

[<span data-ttu-id="39103-138">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="39103-138">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="39103-139">Neu – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="39103-139">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="39103-140">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="39103-140">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="39103-141">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="39103-141">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


