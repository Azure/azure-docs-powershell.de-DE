---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: d8e5f36366df16dd7b0d03fb07f948e436c0a919
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148649"
---
# <span data-ttu-id="ac0a0-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ac0a0-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="ac0a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac0a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ac0a0-103">Generiert erneut anmeldeinformationen für eine Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="ac0a0-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="ac0a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac0a0-104">SYNTAX</span></span>

### <span data-ttu-id="ac0a0-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ac0a0-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac0a0-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac0a0-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac0a0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ac0a0-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac0a0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac0a0-108">DESCRIPTION</span></span>
<span data-ttu-id="ac0a0-109">Das Update-AzContainerRegistryCredential cmdlet generiert erneut anmeldeinformationen für eine Containerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="ac0a0-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="ac0a0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ac0a0-110">EXAMPLES</span></span>

### <span data-ttu-id="ac0a0-111">Beispiel 1: Erneutererieren von Anmeldeinformationen für eine Containerregistrierung</span><span class="sxs-lookup"><span data-stu-id="ac0a0-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="ac0a0-112">Mit diesem Befehl werden anmeldeinformationen für die angegebene Containerregistrierung erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="ac0a0-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="ac0a0-113">Der Administratorbenutzer muss für die Containerregistrierung "MyRegistry" aktiviert sein, \` \` um Anmeldeinformationen erneut erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="ac0a0-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="ac0a0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac0a0-114">PARAMETERS</span></span>

### <span data-ttu-id="ac0a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac0a0-115">-DefaultProfile</span></span>
<span data-ttu-id="ac0a0-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ac0a0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac0a0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ac0a0-117">-Name</span></span>
<span data-ttu-id="ac0a0-118">Containerregistrierungsname.</span><span class="sxs-lookup"><span data-stu-id="ac0a0-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0a0-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="ac0a0-119">-PasswordName</span></span>
<span data-ttu-id="ac0a0-120">Der Name des Kennworts, das erneut generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac0a0-120">The name of password to regenerate.</span></span>
<span data-ttu-id="ac0a0-121">Zulässige Werte: Kennwort, Kennwort2.</span><span class="sxs-lookup"><span data-stu-id="ac0a0-121">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases:
Accepted values: password, password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0a0-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="ac0a0-122">-Registry</span></span>
<span data-ttu-id="ac0a0-123">Containerregistrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="ac0a0-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac0a0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac0a0-124">-ResourceGroupName</span></span>
<span data-ttu-id="ac0a0-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="ac0a0-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0a0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac0a0-126">-ResourceId</span></span>
<span data-ttu-id="ac0a0-127">Die Containerregistrierungsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ac0a0-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac0a0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac0a0-128">-Confirm</span></span>
<span data-ttu-id="ac0a0-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac0a0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac0a0-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ac0a0-130">-WhatIf</span></span>
<span data-ttu-id="ac0a0-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac0a0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac0a0-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac0a0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac0a0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac0a0-133">CommonParameters</span></span>
<span data-ttu-id="ac0a0-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac0a0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac0a0-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac0a0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac0a0-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ac0a0-136">INPUTS</span></span>

### <span data-ttu-id="ac0a0-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ac0a0-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="ac0a0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ac0a0-138">System.String</span></span>

## <span data-ttu-id="ac0a0-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ac0a0-139">OUTPUTS</span></span>

### <span data-ttu-id="ac0a0-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ac0a0-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="ac0a0-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ac0a0-141">NOTES</span></span>

## <span data-ttu-id="ac0a0-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ac0a0-142">RELATED LINKS</span></span>

[<span data-ttu-id="ac0a0-143">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ac0a0-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="ac0a0-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ac0a0-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="ac0a0-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ac0a0-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

