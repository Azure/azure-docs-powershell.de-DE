---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: 267c30c8c10d7c79f8411032016418b1fffd3575
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661376"
---
# <span data-ttu-id="eb333-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="eb333-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="eb333-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eb333-102">SYNOPSIS</span></span>
<span data-ttu-id="eb333-103">Generiert eine Anmeldeinformationen für eine Container Registrierung erneut.</span><span class="sxs-lookup"><span data-stu-id="eb333-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="eb333-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb333-104">SYNTAX</span></span>

### <span data-ttu-id="eb333-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="eb333-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb333-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb333-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb333-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb333-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb333-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eb333-108">DESCRIPTION</span></span>
<span data-ttu-id="eb333-109">Das Update-AzContainerRegistryCredential-Cmdlet generiert eine Anmeldeinformationen für eine Container Registrierung erneut.</span><span class="sxs-lookup"><span data-stu-id="eb333-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="eb333-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb333-110">EXAMPLES</span></span>

### <span data-ttu-id="eb333-111">Beispiel 1: Erneutes Generieren von Anmeldeinformationen für eine Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="eb333-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="eb333-112">Mit diesem Befehl werden Anmeldeinformationen für die angegebene Container Registrierung erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="eb333-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="eb333-113">Administrator Benutzer muss für die Container Registrierung \` myregistry aktiviert sein, um die Anmeldeinformationen erneut \` zu generieren.</span><span class="sxs-lookup"><span data-stu-id="eb333-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="eb333-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="eb333-114">PARAMETERS</span></span>

### <span data-ttu-id="eb333-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb333-115">-DefaultProfile</span></span>
<span data-ttu-id="eb333-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="eb333-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb333-117">-Name</span><span class="sxs-lookup"><span data-stu-id="eb333-117">-Name</span></span>
<span data-ttu-id="eb333-118">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="eb333-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="eb333-119">-Passwordname</span><span class="sxs-lookup"><span data-stu-id="eb333-119">-PasswordName</span></span>
<span data-ttu-id="eb333-120">Der Name des zu regenerierenden Kennworts.</span><span class="sxs-lookup"><span data-stu-id="eb333-120">The name of password to regenerate.</span></span>
<span data-ttu-id="eb333-121">Zulässige Werte: Kennwort, password2.</span><span class="sxs-lookup"><span data-stu-id="eb333-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="eb333-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="eb333-122">-Registry</span></span>
<span data-ttu-id="eb333-123">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="eb333-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="eb333-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb333-124">-ResourceGroupName</span></span>
<span data-ttu-id="eb333-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="eb333-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="eb333-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="eb333-126">-ResourceId</span></span>
<span data-ttu-id="eb333-127">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="eb333-127">The container registry resource id</span></span>

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

### <span data-ttu-id="eb333-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="eb333-128">-Confirm</span></span>
<span data-ttu-id="eb333-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb333-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb333-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb333-130">-WhatIf</span></span>
<span data-ttu-id="eb333-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eb333-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb333-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eb333-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb333-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb333-133">CommonParameters</span></span>
<span data-ttu-id="eb333-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb333-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb333-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb333-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb333-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eb333-136">INPUTS</span></span>

### <span data-ttu-id="eb333-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eb333-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="eb333-138">System. String</span><span class="sxs-lookup"><span data-stu-id="eb333-138">System.String</span></span>

## <span data-ttu-id="eb333-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eb333-139">OUTPUTS</span></span>

### <span data-ttu-id="eb333-140">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="eb333-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="eb333-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="eb333-141">NOTES</span></span>

## <span data-ttu-id="eb333-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eb333-142">RELATED LINKS</span></span>

[<span data-ttu-id="eb333-143">Neu – AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eb333-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="eb333-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="eb333-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="eb333-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="eb333-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

