---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: b5c3ca86129e622a90a84d099961a8f8dd433eef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176112"
---
# <span data-ttu-id="b7c70-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="b7c70-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="b7c70-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7c70-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c70-103">Ruft Bereitstellungsskripts ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="b7c70-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="b7c70-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7c70-104">SYNTAX</span></span>

### <span data-ttu-id="b7c70-105">ListDeploymentScript (Standard)</span><span class="sxs-lookup"><span data-stu-id="b7c70-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7c70-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="b7c70-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7c70-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="b7c70-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7c70-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7c70-108">DESCRIPTION</span></span>
<span data-ttu-id="b7c70-109">Das Cmdlet " **Get-AzDeploymentScript** " Ruft ein einzelnes Bereitstellungsskript oder eine Liste mit Bereitstellungsskripts ab.</span><span class="sxs-lookup"><span data-stu-id="b7c70-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="b7c70-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7c70-110">EXAMPLES</span></span>

### <span data-ttu-id="b7c70-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b7c70-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="b7c70-112">Listet Bereitstellungsskripts im Abonnement im Kontext des aktuellen Benutzers auf.</span><span class="sxs-lookup"><span data-stu-id="b7c70-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="b7c70-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b7c70-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="b7c70-114">Listet Bereitstellungsskripts in der Ressourcengruppe DS-TestRg auf.</span><span class="sxs-lookup"><span data-stu-id="b7c70-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="b7c70-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="b7c70-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="b7c70-116">Ruft ein Bereitstellungsskript mit dem Namen MyDeploymentScript in der Ressourcengruppe DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="b7c70-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="b7c70-117">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="b7c70-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="b7c70-118">Ruft ein Bereitstellungsskript mit der angegebenen Ressourcen-ID ab.</span><span class="sxs-lookup"><span data-stu-id="b7c70-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="b7c70-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7c70-119">PARAMETERS</span></span>

### <span data-ttu-id="b7c70-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c70-120">-DefaultProfile</span></span>
<span data-ttu-id="b7c70-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7c70-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7c70-122">-ID</span><span class="sxs-lookup"><span data-stu-id="b7c70-122">-Id</span></span>
<span data-ttu-id="b7c70-123">Die vollqualifizierte Ressourcen-ID des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="b7c70-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="b7c70-124">Beispiel:/Subscriptions/{subId}/resourceGroups/{rgName}/Providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="b7c70-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c70-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b7c70-125">-Name</span></span>
<span data-ttu-id="b7c70-126">Der Name des Bereitstellungsskripts</span><span class="sxs-lookup"><span data-stu-id="b7c70-126">The name of the deployment script</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c70-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c70-127">-ResourceGroupName</span></span>
<span data-ttu-id="b7c70-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b7c70-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListDeploymentScript
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7c70-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c70-129">CommonParameters</span></span>
<span data-ttu-id="b7c70-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c70-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b7c70-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7c70-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c70-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7c70-132">INPUTS</span></span>

### <span data-ttu-id="b7c70-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c70-133">System.String</span></span>

## <span data-ttu-id="b7c70-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7c70-134">OUTPUTS</span></span>

### <span data-ttu-id="b7c70-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="b7c70-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="b7c70-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7c70-136">NOTES</span></span>

## <span data-ttu-id="b7c70-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7c70-137">RELATED LINKS</span></span>