---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: e65367a94e946aee83df2087463bd0081e925862
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662913"
---
# <span data-ttu-id="beabd-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="beabd-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="beabd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="beabd-102">SYNOPSIS</span></span>
<span data-ttu-id="beabd-103">Generiert eine Anmeldeinformationen für eine Container Registrierung erneut.</span><span class="sxs-lookup"><span data-stu-id="beabd-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="beabd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="beabd-104">SYNTAX</span></span>

### <span data-ttu-id="beabd-105">NameResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="beabd-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="beabd-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="beabd-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="beabd-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="beabd-107">DESCRIPTION</span></span>
<span data-ttu-id="beabd-108">Mit dem Cmdlet **Update-AzureRmContainerRegistryCredential** werden Anmeldeinformationen für eine Container Registrierung erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="beabd-108">The **Update-AzureRmContainerRegistryCredential** cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="beabd-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="beabd-109">EXAMPLES</span></span>

### <span data-ttu-id="beabd-110">Beispiel 1: Erneutes Generieren von Anmeldeinformationen für eine Container Registrierung</span><span class="sxs-lookup"><span data-stu-id="beabd-110">Example 1: Regenerate a login credential for a container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="beabd-111">Mit diesem Befehl werden Anmeldeinformationen für die angegebene Container Registrierung erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="beabd-111">This command regenerates a login credential for the specified container registry.</span></span> <span data-ttu-id="beabd-112">Der Administrator muss für die Container Registrierung aktiviert sein `MyRegistry` , um die Anmeldeinformationen erneut zu generieren.</span><span class="sxs-lookup"><span data-stu-id="beabd-112">Admin user has to be enabled for the container registry `MyRegistry` to regenerate login credentials.</span></span>

## <span data-ttu-id="beabd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="beabd-113">PARAMETERS</span></span>

### <span data-ttu-id="beabd-114">-Name</span><span class="sxs-lookup"><span data-stu-id="beabd-114">-Name</span></span>
<span data-ttu-id="beabd-115">Container Registrierungs Name</span><span class="sxs-lookup"><span data-stu-id="beabd-115">Container Registry Name.</span></span>

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

### <span data-ttu-id="beabd-116">-Passwordname</span><span class="sxs-lookup"><span data-stu-id="beabd-116">-PasswordName</span></span>
<span data-ttu-id="beabd-117">Der Name des zu regenerierenden Kennworts.</span><span class="sxs-lookup"><span data-stu-id="beabd-117">The name of password to regenerate.</span></span>
<span data-ttu-id="beabd-118">Zulässige Werte: Kennwort, password2.</span><span class="sxs-lookup"><span data-stu-id="beabd-118">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beabd-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="beabd-119">-Registry</span></span>
<span data-ttu-id="beabd-120">Container Registrierungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="beabd-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="beabd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beabd-121">-ResourceGroupName</span></span>
<span data-ttu-id="beabd-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="beabd-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="beabd-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="beabd-123">-Confirm</span></span>
<span data-ttu-id="beabd-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="beabd-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beabd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beabd-125">-WhatIf</span></span>
<span data-ttu-id="beabd-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="beabd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beabd-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="beabd-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beabd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beabd-128">-DefaultProfile</span></span>
<span data-ttu-id="beabd-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="beabd-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="beabd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beabd-130">CommonParameters</span></span>
<span data-ttu-id="beabd-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="beabd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beabd-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beabd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beabd-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="beabd-133">INPUTS</span></span>

### <span data-ttu-id="beabd-134">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="beabd-134">PSContainerRegistry</span></span>
<span data-ttu-id="beabd-135">Der Parameter "Registry" akzeptiert den Wert vom Typ "PSContainerRegistry" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="beabd-135">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="beabd-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="beabd-136">OUTPUTS</span></span>

### <span data-ttu-id="beabd-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="beabd-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="beabd-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="beabd-138">NOTES</span></span>

## <span data-ttu-id="beabd-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="beabd-139">RELATED LINKS</span></span>

[<span data-ttu-id="beabd-140">Neu – AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="beabd-140">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="beabd-141">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="beabd-141">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="beabd-142">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="beabd-142">Get-AzureRmContainerRegistryCredential</span></span>](./Get-AzureRmContainerRegistryCredential.md)

