---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0143CE35-3B1D-4829-B880-A5CA25B83883
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Test-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: b357215bf2c4ba032ca44e37cc445e12606aeffe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496925"
---
# <span data-ttu-id="8a968-101">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8a968-101">Test-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="8a968-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a968-102">SYNOPSIS</span></span>
<span data-ttu-id="8a968-103">Überprüft eine Ressourcengruppen Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="8a968-103">Validates a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a968-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a968-104">SYNTAX</span></span>

### <span data-ttu-id="8a968-105">Bereitstellung über Vorlagendatei ohne Parameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a968-105">Deployment via template file without parameters (Default)</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateFile <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a968-106">Bereitstellung über Vorlagendatei-und Vorlagenparameter Objekt</span><span class="sxs-lookup"><span data-stu-id="8a968-106">Deployment via template file and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a968-107">Bereitstellung über Vorlagen-URI und Vorlagenparameter-Objekt</span><span class="sxs-lookup"><span data-stu-id="8a968-107">Deployment via template uri and template parameters object</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterObject <Hashtable> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a968-108">Bereitstellung über Vorlagendatei-und Vorlagenparameter Datei</span><span class="sxs-lookup"><span data-stu-id="8a968-108">Deployment via template file and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a968-109">Bereitstellung über Vorlagen-URI und Vorlagenparameter-Datei</span><span class="sxs-lookup"><span data-stu-id="8a968-109">Deployment via template uri and template parameters file</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterFile <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a968-110">Bereitstellung über Vorlagen-Datei Vorlagenparameter-URI</span><span class="sxs-lookup"><span data-stu-id="8a968-110">Deployment via template file template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateFile <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a968-111">Bereitstellung über Vorlagen-URI und Vorlagenparameter-URI</span><span class="sxs-lookup"><span data-stu-id="8a968-111">Deployment via template uri and template parameters uri</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>]
 -TemplateParameterUri <String> -TemplateUri <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a968-112">Bereitstellung über Vorlagen-URI ohne Parameter</span><span class="sxs-lookup"><span data-stu-id="8a968-112">Deployment via template uri without parameters</span></span>
```
Test-AzureRmResourceGroupDeployment -ResourceGroupName <String> [-Mode <DeploymentMode>] -TemplateUri <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a968-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a968-113">DESCRIPTION</span></span>
<span data-ttu-id="8a968-114">Das Cmdlet **Test-AzureRmResourceGroupDeployment** bestimmt, ob eine Azure Resource Group-Bereitstellungsvorlage und deren Parameterwerte gültig sind.</span><span class="sxs-lookup"><span data-stu-id="8a968-114">The **Test-AzureRmResourceGroupDeployment** cmdlet determines whether an Azure resource group deployment template and its parameter values are valid.</span></span>

## <span data-ttu-id="8a968-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a968-115">EXAMPLES</span></span>

## <span data-ttu-id="8a968-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a968-116">PARAMETERS</span></span>

### <span data-ttu-id="8a968-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8a968-117">-ApiVersion</span></span>
<span data-ttu-id="8a968-118">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8a968-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8a968-119">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="8a968-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8a968-120">-Modus</span><span class="sxs-lookup"><span data-stu-id="8a968-120">-Mode</span></span>
<span data-ttu-id="8a968-121">Gibt den Bereitstellungsmodus an.</span><span class="sxs-lookup"><span data-stu-id="8a968-121">Specifies the deployment mode.</span></span>
<span data-ttu-id="8a968-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8a968-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a968-123">Inkrementelle</span><span class="sxs-lookup"><span data-stu-id="8a968-123">Incremental</span></span>
- <span data-ttu-id="8a968-124">Komplette</span><span class="sxs-lookup"><span data-stu-id="8a968-124">Complete</span></span>

```yaml
Type: Microsoft.Azure.Management.ResourceManager.Models.DeploymentMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a968-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="8a968-125">-Pre</span></span>
<span data-ttu-id="8a968-126">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8a968-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8a968-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a968-127">-ResourceGroupName</span></span>
<span data-ttu-id="8a968-128">Gibt den Namen der zu testenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8a968-128">Specifies the name of the resource group to test.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a968-129">-Vorlagendatei</span><span class="sxs-lookup"><span data-stu-id="8a968-129">-TemplateFile</span></span>
<span data-ttu-id="8a968-130">Gibt den vollständigen Pfad einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="8a968-130">Specifies the full path of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file without parameters, Deployment via template file and template parameters object, Deployment via template file and template parameters file, Deployment via template file template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a968-131">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="8a968-131">-TemplateParameterFile</span></span>
<span data-ttu-id="8a968-132">Gibt den vollständigen Pfad einer JSON-Datei an, die die Namen und Werte der Vorlagenparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="8a968-132">Specifies the full path of a JSON file that contains the names and values of the template parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file and template parameters file, Deployment via template uri and template parameters file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a968-133">-TemplateParameterObject</span><span class="sxs-lookup"><span data-stu-id="8a968-133">-TemplateParameterObject</span></span>
<span data-ttu-id="8a968-134">Gibt eine Hashtabelle mit Vorlagenparameter Namen und-Werten an.</span><span class="sxs-lookup"><span data-stu-id="8a968-134">Specifies a hash table of template parameter names and values.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Deployment via template file and template parameters object, Deployment via template uri and template parameters object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a968-135">-TemplateParameterUri</span><span class="sxs-lookup"><span data-stu-id="8a968-135">-TemplateParameterUri</span></span>
<span data-ttu-id="8a968-136">Gibt den URI einer Vorlagenparameter Datei an.</span><span class="sxs-lookup"><span data-stu-id="8a968-136">Specifies the URI of a template parameters file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template file template parameters uri, Deployment via template uri and template parameters uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a968-137">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="8a968-137">-TemplateUri</span></span>
<span data-ttu-id="8a968-138">Gibt den URI einer JSON-Vorlagendatei an.</span><span class="sxs-lookup"><span data-stu-id="8a968-138">Specifies the URI of a JSON template file.</span></span>

```yaml
Type: System.String
Parameter Sets: Deployment via template uri and template parameters object, Deployment via template uri and template parameters file, Deployment via template uri and template parameters uri, Deployment via template uri without parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a968-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a968-139">-DefaultProfile</span></span>
<span data-ttu-id="8a968-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a968-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a968-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a968-141">CommonParameters</span></span>
<span data-ttu-id="8a968-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a968-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a968-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a968-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a968-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a968-144">INPUTS</span></span>

## <span data-ttu-id="8a968-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a968-145">OUTPUTS</span></span>

### <span data-ttu-id="8a968-146">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResourceManagerError]</span><span class="sxs-lookup"><span data-stu-id="8a968-146">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceManagerError]</span></span>

## <span data-ttu-id="8a968-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a968-147">NOTES</span></span>

## <span data-ttu-id="8a968-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a968-148">RELATED LINKS</span></span>

[<span data-ttu-id="8a968-149">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8a968-149">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8a968-150">Neu – AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8a968-150">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8a968-151">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8a968-151">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8a968-152">Stopp-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8a968-152">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)


