---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: 4cdc70928f2b27ae1e1604c52e5703798a302a66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502453"
---
# <span data-ttu-id="43375-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="43375-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="43375-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43375-102">SYNOPSIS</span></span>
<span data-ttu-id="43375-103">Bricht die Bereitstellung einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="43375-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43375-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="43375-104">SYNTAX</span></span>

### <span data-ttu-id="43375-105">StopByResourceGroupDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="43375-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43375-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="43375-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43375-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43375-107">DESCRIPTION</span></span>
<span data-ttu-id="43375-108">Das Cmdlet " **Stop-AzureRmResourceGroupDeployment** " bricht eine Azure Resource Group-Bereitstellung ab, die gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="43375-108">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="43375-109">Damit eine Bereitstellung beendet werden kann, muss die Bereitstellung einen unvollständigen Bereitstellungsstatus aufweisen, beispielsweise die Bereitstellung und nicht den Status abgeschlossen, wie bereitgestellt oder fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="43375-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="43375-110">Eine Azure-Ressource ist eine vom Benutzer verwaltete Entität, beispielsweise eine Website, eine Datenbank oder ein Datenbankserver.</span><span class="sxs-lookup"><span data-stu-id="43375-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="43375-111">Eine Ressourcengruppe ist eine Sammlung von Ressourcen, die als Einheit bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="43375-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="43375-112">Verwenden Sie das New-AzureRmResourceGroupDeployment-Cmdlet, um eine Ressourcengruppe bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="43375-112">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="43375-113">Das New-AzureRmResource-Cmdlet erstellt eine neue Ressource, löst aber keinen Bereitstellungsvorgang der Ressourcengruppe aus, den dieses Cmdlet beenden kann.</span><span class="sxs-lookup"><span data-stu-id="43375-113">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="43375-114">Dieses Cmdlet beendet nur eine ausgeführte Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="43375-114">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="43375-115">Verwenden Sie den Parameter *Name* , um eine bestimmte Bereitstellung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="43375-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="43375-116">Wenn Sie den Parameter *Name* nicht angeben, sucht **Stop-AzureRmResourceGroupDeployment** nach einer ausgeführten Bereitstellung und beendet Sie.</span><span class="sxs-lookup"><span data-stu-id="43375-116">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="43375-117">Wenn das Cmdlet mehr als eine ausgeführte Bereitstellung findet, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="43375-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="43375-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43375-118">EXAMPLES</span></span>

## <span data-ttu-id="43375-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="43375-119">PARAMETERS</span></span>

### <span data-ttu-id="43375-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="43375-120">-ApiVersion</span></span>
<span data-ttu-id="43375-121">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="43375-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="43375-122">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="43375-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="43375-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43375-123">-DefaultProfile</span></span>
<span data-ttu-id="43375-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="43375-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43375-125">-ID</span><span class="sxs-lookup"><span data-stu-id="43375-125">-Id</span></span>
<span data-ttu-id="43375-126">Gibt die ID der Bereitstellung der Ressourcengruppe an, die beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43375-126">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43375-127">-Name</span><span class="sxs-lookup"><span data-stu-id="43375-127">-Name</span></span>
<span data-ttu-id="43375-128">Gibt den Namen der Bereitstellung der Ressourcengruppe an, die beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43375-128">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="43375-129">Wenn Sie diesen Parameter nicht angeben, sucht dieses Cmdlet nach einer ausgeführten Bereitstellung in der Ressourcengruppe und beendet Sie.</span><span class="sxs-lookup"><span data-stu-id="43375-129">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="43375-130">Wenn Sie mehr als eine ausgeführte Bereitstellung findet, schlägt der Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="43375-130">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="43375-131">Verwenden Sie das Get-AzureRmResourceGroupDeployment-Cmdlet, um den Bereitstellungsnamen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="43375-131">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43375-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="43375-132">-Pre</span></span>
<span data-ttu-id="43375-133">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="43375-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="43375-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43375-134">-ResourceGroupName</span></span>
<span data-ttu-id="43375-135">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="43375-135">Specifies the name of the resource group.</span></span>
<span data-ttu-id="43375-136">Dieses Cmdlet beendet die Bereitstellung der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="43375-136">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43375-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="43375-137">-Confirm</span></span>
<span data-ttu-id="43375-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43375-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43375-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43375-139">-WhatIf</span></span>
<span data-ttu-id="43375-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43375-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43375-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43375-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43375-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43375-142">CommonParameters</span></span>
<span data-ttu-id="43375-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43375-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43375-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43375-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43375-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43375-145">INPUTS</span></span>

### <span data-ttu-id="43375-146">Keine</span><span class="sxs-lookup"><span data-stu-id="43375-146">None</span></span>

## <span data-ttu-id="43375-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43375-147">OUTPUTS</span></span>

### <span data-ttu-id="43375-148">Boolean</span><span class="sxs-lookup"><span data-stu-id="43375-148">Boolean</span></span>

## <span data-ttu-id="43375-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="43375-149">NOTES</span></span>

## <span data-ttu-id="43375-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43375-150">RELATED LINKS</span></span>

[<span data-ttu-id="43375-151">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="43375-151">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="43375-152">Neu – AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="43375-152">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="43375-153">Neu – AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="43375-153">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="43375-154">Neu – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="43375-154">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="43375-155">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="43375-155">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="43375-156">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="43375-156">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


