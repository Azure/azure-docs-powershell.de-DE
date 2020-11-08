---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176469"
---
# <span data-ttu-id="51539-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="51539-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="51539-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51539-102">SYNOPSIS</span></span>
<span data-ttu-id="51539-103">Erstellt eine neue CDN-Ursprungsgruppe</span><span class="sxs-lookup"><span data-stu-id="51539-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="51539-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51539-104">SYNTAX</span></span>

### <span data-ttu-id="51539-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="51539-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51539-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51539-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51539-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51539-107">DESCRIPTION</span></span>
<span data-ttu-id="51539-108">Mit dem New-AzCdnOriginGroup wird eine neue Ursprungsgruppe innerhalb des angegebenen Endpunkts erstellt.</span><span class="sxs-lookup"><span data-stu-id="51539-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="51539-109">Wenn es sich um die erste Ursprungsgruppe für den Endpunkt handelt, muss auch die DefaultOriginGroup-Eigenschaft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="51539-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="51539-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51539-110">EXAMPLES</span></span>

### <span data-ttu-id="51539-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="51539-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="51539-112">Mit diesem Cmdlet wird eine neue Ursprungsgruppe innerhalb des angegebenen Endpunkts erstellt.</span><span class="sxs-lookup"><span data-stu-id="51539-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="51539-113">Sie verwendet die angegebenen Ursprungs-IDs als Satz von Ursprüngen.</span><span class="sxs-lookup"><span data-stu-id="51539-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="51539-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="51539-114">PARAMETERS</span></span>

### <span data-ttu-id="51539-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="51539-115">-CdnOriginGroup</span></span>
<span data-ttu-id="51539-116">Das CDN-Ursprungs Gruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="51539-116">The CDN origin group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.OriginGroup.PSOriginGroup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51539-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51539-117">-DefaultProfile</span></span>
<span data-ttu-id="51539-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51539-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51539-119">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="51539-119">-EndpointName</span></span>
<span data-ttu-id="51539-120">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="51539-120">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51539-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="51539-121">-OriginGroupName</span></span>
<span data-ttu-id="51539-122">Name der Azure CDN-Ursprungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="51539-122">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51539-123">-Origin-Nr</span><span class="sxs-lookup"><span data-stu-id="51539-123">-OriginId</span></span>
<span data-ttu-id="51539-124">Azure CDN-Ursprungs Gruppen-IDs.</span><span class="sxs-lookup"><span data-stu-id="51539-124">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51539-125">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="51539-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="51539-126">Die Anzahl von Sekunden zwischen Integritätsprüfungen.</span><span class="sxs-lookup"><span data-stu-id="51539-126">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51539-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="51539-127">-ProbePath</span></span>
<span data-ttu-id="51539-128">Der Pfad relativ zum Ursprung, der verwendet wird, um den Zustand des Ursprungs zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="51539-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51539-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="51539-129">-ProbeProtocol</span></span>
<span data-ttu-id="51539-130">Protokoll, das für die Integritätsprüfung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51539-130">Protocol to use for health probe.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51539-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="51539-131">-ProbeRequestType</span></span>
<span data-ttu-id="51539-132">Der Typ der ausgestellten Integritäts Prüfpunktanforderung.</span><span class="sxs-lookup"><span data-stu-id="51539-132">The type of health probe request that is made.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51539-133">-Profilname</span><span class="sxs-lookup"><span data-stu-id="51539-133">-ProfileName</span></span>
<span data-ttu-id="51539-134">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="51539-134">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51539-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51539-135">-ResourceGroupName</span></span>
<span data-ttu-id="51539-136">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="51539-136">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51539-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="51539-137">-Confirm</span></span>
<span data-ttu-id="51539-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51539-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51539-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51539-139">-WhatIf</span></span>
<span data-ttu-id="51539-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51539-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51539-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51539-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51539-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51539-142">CommonParameters</span></span>
<span data-ttu-id="51539-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51539-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51539-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51539-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51539-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51539-145">INPUTS</span></span>

### <span data-ttu-id="51539-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="51539-146">System.Object</span></span>

## <span data-ttu-id="51539-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51539-147">OUTPUTS</span></span>

### <span data-ttu-id="51539-148">System. Object</span><span class="sxs-lookup"><span data-stu-id="51539-148">System.Object</span></span>

## <span data-ttu-id="51539-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="51539-149">NOTES</span></span>

## <span data-ttu-id="51539-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51539-150">RELATED LINKS</span></span>
