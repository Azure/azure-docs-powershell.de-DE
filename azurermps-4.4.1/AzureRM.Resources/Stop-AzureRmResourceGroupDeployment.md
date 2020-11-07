---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: f07b2f59f1a38aca780e1e869bb3904725df6dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664983"
---
# <span data-ttu-id="d80a8-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d80a8-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="d80a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d80a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d80a8-103">Bricht die Bereitstellung einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="d80a8-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d80a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d80a8-104">SYNTAX</span></span>

### <span data-ttu-id="d80a8-105">Der Parametersatz für den Bereitstellungsnamen.</span><span class="sxs-lookup"><span data-stu-id="d80a8-105">The deployment name parameter set.</span></span> <span data-ttu-id="d80a8-106">Standard</span><span class="sxs-lookup"><span data-stu-id="d80a8-106">(Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d80a8-107">Der Parametersatz für die Bereitstellungs-ID.</span><span class="sxs-lookup"><span data-stu-id="d80a8-107">The deployment Id parameter set.</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d80a8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d80a8-108">DESCRIPTION</span></span>
<span data-ttu-id="d80a8-109">Das Cmdlet " **Stop-AzureRmResourceGroupDeployment** " bricht eine Azure Resource Group-Bereitstellung ab, die gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="d80a8-109">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="d80a8-110">Damit eine Bereitstellung beendet werden kann, muss die Bereitstellung einen unvollständigen Bereitstellungsstatus aufweisen, beispielsweise die Bereitstellung und nicht den Status abgeschlossen, wie bereitgestellt oder fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="d80a8-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="d80a8-111">Eine Azure-Ressource ist eine vom Benutzer verwaltete Entität, beispielsweise eine Website, eine Datenbank oder ein Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="d80a8-111">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="d80a8-112">Eine Ressourcengruppe ist eine Sammlung von Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d80a8-112">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="d80a8-113">Verwenden Sie das New-AzureRmResourceGroupDeployment-Cmdlet, um eine Ressourcengruppe bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d80a8-113">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="d80a8-114">Das New-AzureRmResource-Cmdlet erstellt eine neue Ressource, löst aber keinen Bereitstellungsvorgang der Ressourcengruppe aus, den dieses Cmdlet beenden kann.</span><span class="sxs-lookup"><span data-stu-id="d80a8-114">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="d80a8-115">Dieses Cmdlet beendet nur eine ausgeführte Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="d80a8-115">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="d80a8-116">Verwenden Sie den Parameter *Name* , um eine bestimmte Bereitstellung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="d80a8-116">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="d80a8-117">Wenn Sie den Parameter *Name* nicht angeben, sucht **Stop-AzureRmResourceGroupDeployment** nach einer ausgeführten Bereitstellung und beendet Sie.</span><span class="sxs-lookup"><span data-stu-id="d80a8-117">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="d80a8-118">Wenn das Cmdlet mehr als eine ausgeführte Bereitstellung findet, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="d80a8-118">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="d80a8-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d80a8-119">EXAMPLES</span></span>

## <span data-ttu-id="d80a8-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="d80a8-120">PARAMETERS</span></span>

### <span data-ttu-id="d80a8-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d80a8-121">-ApiVersion</span></span>
<span data-ttu-id="d80a8-122">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d80a8-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="d80a8-123">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="d80a8-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="d80a8-124">-ID</span><span class="sxs-lookup"><span data-stu-id="d80a8-124">-Id</span></span>
<span data-ttu-id="d80a8-125">Gibt die ID der Bereitstellung der Ressourcengruppe an, die beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d80a8-125">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="d80a8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d80a8-126">-Name</span></span>
<span data-ttu-id="d80a8-127">Gibt den Namen der Bereitstellung der Ressourcengruppe an, die beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d80a8-127">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="d80a8-128">Wenn Sie diesen Parameter nicht angeben, sucht dieses Cmdlet nach einer ausgeführten Bereitstellung in der Ressourcengruppe und beendet Sie.</span><span class="sxs-lookup"><span data-stu-id="d80a8-128">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="d80a8-129">Wenn Sie mehr als eine ausgeführte Bereitstellung findet, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="d80a8-129">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="d80a8-130">Verwenden Sie das Get-AzureRmResourceGroupDeployment-Cmdlet, um den Bereitstellungsnamen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d80a8-130">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d80a8-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="d80a8-131">-Pre</span></span>
<span data-ttu-id="d80a8-132">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d80a8-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d80a8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d80a8-133">-ResourceGroupName</span></span>
<span data-ttu-id="d80a8-134">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="d80a8-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="d80a8-135">Dieses Cmdlet beendet die Bereitstellung der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d80a8-135">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d80a8-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d80a8-136">-Confirm</span></span>
<span data-ttu-id="d80a8-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d80a8-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d80a8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d80a8-138">-WhatIf</span></span>
<span data-ttu-id="d80a8-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d80a8-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d80a8-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d80a8-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d80a8-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d80a8-141">-DefaultProfile</span></span>
<span data-ttu-id="d80a8-142">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d80a8-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d80a8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80a8-143">CommonParameters</span></span>
<span data-ttu-id="d80a8-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d80a8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80a8-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d80a8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80a8-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d80a8-146">INPUTS</span></span>

### <span data-ttu-id="d80a8-147">Keine</span><span class="sxs-lookup"><span data-stu-id="d80a8-147">None</span></span>

## <span data-ttu-id="d80a8-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d80a8-148">OUTPUTS</span></span>

### <span data-ttu-id="d80a8-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="d80a8-149">Boolean</span></span>

## <span data-ttu-id="d80a8-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="d80a8-150">NOTES</span></span>

## <span data-ttu-id="d80a8-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d80a8-151">RELATED LINKS</span></span>

[<span data-ttu-id="d80a8-152">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d80a8-152">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d80a8-153">Neu – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d80a8-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="d80a8-154">Neu – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d80a8-154">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="d80a8-155">Neu – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d80a8-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d80a8-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d80a8-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="d80a8-157">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d80a8-157">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


