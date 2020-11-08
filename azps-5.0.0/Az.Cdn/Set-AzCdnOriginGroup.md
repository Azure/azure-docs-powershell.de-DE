---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177845"
---
# <span data-ttu-id="003e0-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="003e0-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="003e0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="003e0-102">SYNOPSIS</span></span>
<span data-ttu-id="003e0-103">Aktualisiert die CDN-Ursprungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="003e0-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="003e0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="003e0-104">SYNTAX</span></span>

### <span data-ttu-id="003e0-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="003e0-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="003e0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="003e0-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="003e0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="003e0-107">DESCRIPTION</span></span>
<span data-ttu-id="003e0-108">Set-AzCdnOriginGroup aktualisiert die angegebene Ursprungsgruppe innerhalb des angegebenen Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="003e0-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="003e0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="003e0-109">EXAMPLES</span></span>

### <span data-ttu-id="003e0-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="003e0-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="003e0-111">Mit diesem Cmdlet wird die ProbeIntervalInSeconds-Eigenschaft in der Gruppe Ursprung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="003e0-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="003e0-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="003e0-112">PARAMETERS</span></span>

### <span data-ttu-id="003e0-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="003e0-113">-CdnOriginGroup</span></span>
<span data-ttu-id="003e0-114">Das CDN-Ursprungs Gruppenobjekt.</span><span class="sxs-lookup"><span data-stu-id="003e0-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="003e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003e0-115">-DefaultProfile</span></span>
<span data-ttu-id="003e0-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="003e0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="003e0-117">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="003e0-117">-EndpointName</span></span>
<span data-ttu-id="003e0-118">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="003e0-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="003e0-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="003e0-119">-OriginGroupName</span></span>
<span data-ttu-id="003e0-120">Name der Azure CDN-Ursprungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="003e0-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="003e0-121">-Origin-Nr</span><span class="sxs-lookup"><span data-stu-id="003e0-121">-OriginId</span></span>
<span data-ttu-id="003e0-122">Azure CDN-Ursprungs Gruppen-IDs.</span><span class="sxs-lookup"><span data-stu-id="003e0-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="003e0-123">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="003e0-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="003e0-124">Die Anzahl von Sekunden zwischen Integritätsprüfungen.</span><span class="sxs-lookup"><span data-stu-id="003e0-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="003e0-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="003e0-125">-ProbePath</span></span>
<span data-ttu-id="003e0-126">Der Pfad relativ zum Ursprung, der verwendet wird, um den Zustand des Ursprungs zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="003e0-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="003e0-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="003e0-127">-ProbeProtocol</span></span>
<span data-ttu-id="003e0-128">Protokoll, das für die Integritätsprüfung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="003e0-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="003e0-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="003e0-129">-ProbeRequestType</span></span>
<span data-ttu-id="003e0-130">Der Typ der ausgestellten Integritäts Prüfpunktanforderung.</span><span class="sxs-lookup"><span data-stu-id="003e0-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="003e0-131">-Profilname</span><span class="sxs-lookup"><span data-stu-id="003e0-131">-ProfileName</span></span>
<span data-ttu-id="003e0-132">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="003e0-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="003e0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="003e0-133">-ResourceGroupName</span></span>
<span data-ttu-id="003e0-134">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="003e0-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="003e0-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="003e0-135">-Confirm</span></span>
<span data-ttu-id="003e0-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="003e0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="003e0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="003e0-137">-WhatIf</span></span>
<span data-ttu-id="003e0-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="003e0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="003e0-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="003e0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="003e0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003e0-140">CommonParameters</span></span>
<span data-ttu-id="003e0-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="003e0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003e0-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="003e0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003e0-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="003e0-143">INPUTS</span></span>

### <span data-ttu-id="003e0-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="003e0-144">System.Object</span></span>

## <span data-ttu-id="003e0-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="003e0-145">OUTPUTS</span></span>

### <span data-ttu-id="003e0-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="003e0-146">System.Object</span></span>

## <span data-ttu-id="003e0-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="003e0-147">NOTES</span></span>

## <span data-ttu-id="003e0-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="003e0-148">RELATED LINKS</span></span>
