---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 836e8983a9d2e6c7ff21444f0da7b3bf85c1b1d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504450"
---
# <span data-ttu-id="904ec-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="904ec-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="904ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="904ec-102">SYNOPSIS</span></span>
<span data-ttu-id="904ec-103">Generiert eine Anmeldeinformationen für eine Container Registrierung erneut.</span><span class="sxs-lookup"><span data-stu-id="904ec-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="904ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="904ec-104">SYNTAX</span></span>

### <span data-ttu-id="904ec-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="904ec-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="904ec-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="904ec-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="904ec-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="904ec-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="904ec-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="904ec-108">DESCRIPTION</span></span>
<span data-ttu-id="904ec-109">Das Update-AzureRmContainerRegistryCredential-Cmdlet generiert eine Anmeldeinformationen für eine Container Registrierung erneut.</span><span class="sxs-lookup"><span data-stu-id="904ec-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="904ec-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="904ec-110">EXAMPLES</span></span>

### <span data-ttu-id="904ec-111">Beispiel 1: Erneutes Generieren von Anmeldeinformationen für eine Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="904ec-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="904ec-112">Mit diesem Befehl werden Anmeldeinformationen für die angegebene Container Registrierung erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="904ec-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="904ec-113">Administrator Benutzer muss für die Container Registrierung \` myregistry aktiviert sein, um die Anmeldeinformationen erneut \` zu generieren.</span><span class="sxs-lookup"><span data-stu-id="904ec-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="904ec-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="904ec-114">PARAMETERS</span></span>

### <span data-ttu-id="904ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="904ec-115">-DefaultProfile</span></span>
<span data-ttu-id="904ec-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="904ec-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="904ec-117">-Name</span><span class="sxs-lookup"><span data-stu-id="904ec-117">-Name</span></span>
<span data-ttu-id="904ec-118">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="904ec-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="904ec-119">-Passwordname</span><span class="sxs-lookup"><span data-stu-id="904ec-119">-PasswordName</span></span>
<span data-ttu-id="904ec-120">Der Name des zu regenerierenden Kennworts.</span><span class="sxs-lookup"><span data-stu-id="904ec-120">The name of password to regenerate.</span></span>
<span data-ttu-id="904ec-121">Zulässige Werte: Kennwort, password2.</span><span class="sxs-lookup"><span data-stu-id="904ec-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="904ec-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="904ec-122">-Registry</span></span>
<span data-ttu-id="904ec-123">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="904ec-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="904ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="904ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="904ec-125">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="904ec-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="904ec-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="904ec-126">-ResourceId</span></span>
<span data-ttu-id="904ec-127">Die Ressourcen-ID der Container-Registrierung</span><span class="sxs-lookup"><span data-stu-id="904ec-127">The container registry resource id</span></span>

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

### <span data-ttu-id="904ec-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="904ec-128">-Confirm</span></span>
<span data-ttu-id="904ec-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="904ec-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="904ec-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="904ec-130">-WhatIf</span></span>
<span data-ttu-id="904ec-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="904ec-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="904ec-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="904ec-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="904ec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="904ec-133">CommonParameters</span></span>
<span data-ttu-id="904ec-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="904ec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="904ec-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="904ec-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="904ec-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="904ec-136">INPUTS</span></span>

### <span data-ttu-id="904ec-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="904ec-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="904ec-138">Parameter: Registrierung (ByValue)</span><span class="sxs-lookup"><span data-stu-id="904ec-138">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="904ec-139">System. String</span><span class="sxs-lookup"><span data-stu-id="904ec-139">System.String</span></span>

## <span data-ttu-id="904ec-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="904ec-140">OUTPUTS</span></span>

### <span data-ttu-id="904ec-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="904ec-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="904ec-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="904ec-142">NOTES</span></span>

## <span data-ttu-id="904ec-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="904ec-143">RELATED LINKS</span></span>

[<span data-ttu-id="904ec-144">Neu – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="904ec-144">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="904ec-145">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="904ec-145">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="904ec-146">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="904ec-146">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

