---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzSecurityPartnerProvider.md
ms.openlocfilehash: a51345653580261178191687f54bf0f2a8cc6f0c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169668"
---
# <span data-ttu-id="ce122-101">Remove-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ce122-101">Remove-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="ce122-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce122-102">SYNOPSIS</span></span>
<span data-ttu-id="ce122-103">Löscht einen Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="ce122-103">Deletes an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="ce122-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce122-104">SYNTAX</span></span>

### <span data-ttu-id="ce122-105">SecurityPartnerProviderNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce122-105">SecurityPartnerProviderNameParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce122-106">SecurityPartnerProviderInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce122-106">SecurityPartnerProviderInputObjectParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -SecurityPartnerProvider <PSSecurityPartnerProvider> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce122-107">SecurityPartnerProviderResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce122-107">SecurityPartnerProviderResourceIdParameterSet</span></span>
```
Remove-AzSecurityPartnerProvider -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce122-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce122-108">DESCRIPTION</span></span>
<span data-ttu-id="ce122-109">Das **Cmdlet "Remove-AzSecurityPartnerProvider"** löscht einen Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ce122-109">The **Remove-AzSecurityPartnerProvider** cmdlet deletes an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="ce122-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ce122-110">EXAMPLES</span></span>

### <span data-ttu-id="ce122-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ce122-111">Example 1</span></span>
```powershell
Remove-AzSecurityPartnerProvider -ResourceGroupName securityPartnerProviderRG -Name securityPartnerProvider
```

## <span data-ttu-id="ce122-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce122-112">PARAMETERS</span></span>

### <span data-ttu-id="ce122-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce122-113">-AsJob</span></span>
<span data-ttu-id="ce122-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="ce122-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce122-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce122-115">-DefaultProfile</span></span>
<span data-ttu-id="ce122-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce122-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce122-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ce122-117">-Force</span></span>
<span data-ttu-id="ce122-118">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="ce122-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ce122-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ce122-119">-Name</span></span>
<span data-ttu-id="ce122-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="ce122-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce122-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce122-121">-PassThru</span></span>
<span data-ttu-id="ce122-122">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce122-122">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="ce122-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce122-123">-ResourceGroupName</span></span>
<span data-ttu-id="ce122-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ce122-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce122-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce122-125">-ResourceId</span></span>
<span data-ttu-id="ce122-126">Die Ressourcen-ID von securityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="ce122-126">The securityPartnerProvider resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SecurityPartnerProviderResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce122-127">-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ce122-127">-SecurityPartnerProvider</span></span>
<span data-ttu-id="ce122-128">Das Eingabeobjekt "securityPartnerProvider".</span><span class="sxs-lookup"><span data-stu-id="ce122-128">The securityPartnerProvider input object.</span></span>

```yaml
Type: PSSecurityPartnerProvider
Parameter Sets: SecurityPartnerProviderInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce122-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce122-129">-Confirm</span></span>
<span data-ttu-id="ce122-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce122-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce122-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ce122-131">-WhatIf</span></span>
<span data-ttu-id="ce122-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce122-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce122-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce122-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce122-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce122-134">CommonParameters</span></span>
<span data-ttu-id="ce122-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce122-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce122-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce122-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce122-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ce122-137">INPUTS</span></span>

### <span data-ttu-id="ce122-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ce122-138">System.String</span></span>

### <span data-ttu-id="ce122-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="ce122-139">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="ce122-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ce122-140">OUTPUTS</span></span>

### <span data-ttu-id="ce122-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ce122-141">System.Boolean</span></span>

## <span data-ttu-id="ce122-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ce122-142">NOTES</span></span>

## <span data-ttu-id="ce122-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ce122-143">RELATED LINKS</span></span>
