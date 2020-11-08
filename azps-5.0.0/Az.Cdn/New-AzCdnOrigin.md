---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176471"
---
# <span data-ttu-id="2cfaf-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2cfaf-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="2cfaf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2cfaf-102">SYNOPSIS</span></span>
<span data-ttu-id="2cfaf-103">Erstellt einen neuen CDN-Ursprung</span><span class="sxs-lookup"><span data-stu-id="2cfaf-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="2cfaf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cfaf-104">SYNTAX</span></span>

### <span data-ttu-id="2cfaf-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2cfaf-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2cfaf-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cfaf-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2cfaf-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cfaf-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2cfaf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cfaf-108">DESCRIPTION</span></span>
<span data-ttu-id="2cfaf-109">Die New-AzCdnOrigin erstellt einen neuen CDN-Ursprung innerhalb des angegebenen Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="2cfaf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2cfaf-110">EXAMPLES</span></span>

### <span data-ttu-id="2cfaf-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2cfaf-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="2cfaf-112">Mit diesem Cmdlet wird ein neuer CDN-Ursprung für den angegebenen Endpunkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="2cfaf-113">Dabei wird der angegebene Hostname als Ursprung verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="2cfaf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cfaf-114">PARAMETERS</span></span>

### <span data-ttu-id="2cfaf-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2cfaf-115">-CdnOrigin</span></span>
<span data-ttu-id="2cfaf-116">Das CDN-Ursprungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cfaf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cfaf-117">-DefaultProfile</span></span>
<span data-ttu-id="2cfaf-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cfaf-119">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="2cfaf-119">-EndpointName</span></span>
<span data-ttu-id="2cfaf-120">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-120">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfaf-121">-Hostname</span><span class="sxs-lookup"><span data-stu-id="2cfaf-121">-HostName</span></span>
<span data-ttu-id="2cfaf-122">Azure CDN-Ursprungshost Name.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-122">Azure CDN origin host name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfaf-123">-Wert von HTTPPort</span><span class="sxs-lookup"><span data-stu-id="2cfaf-123">-HttpPort</span></span>
<span data-ttu-id="2cfaf-124">Azure CDN Origin-HTTP-Port.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-124">Azure CDN origin http port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfaf-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="2cfaf-125">-HttpsPort</span></span>
<span data-ttu-id="2cfaf-126">Azure CDN-Ursprungs HTTPS-Port.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-126">Azure CDN origin https port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfaf-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="2cfaf-127">-OriginHostHeader</span></span>
<span data-ttu-id="2cfaf-128">Azure CDN-Ursprungshost Header.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-128">Azure CDN origin host header.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfaf-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="2cfaf-129">-OriginName</span></span>
<span data-ttu-id="2cfaf-130">Azure CDN-Ursprungsname.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-130">Azure CDN origin name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfaf-131">-Priorität</span><span class="sxs-lookup"><span data-stu-id="2cfaf-131">-Priority</span></span>
<span data-ttu-id="2cfaf-132">Azure CDN-Ursprungs Priorität.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-132">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfaf-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="2cfaf-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="2cfaf-134">Eine benutzerdefinierte Nachricht, die in die Genehmigungsanforderung aufgenommen werden soll, um eine Verbindung mit dem privaten Link herzustellen.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfaf-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="2cfaf-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="2cfaf-136">Azure CDN Origin-Speicherort für private Links.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-136">Azure CDN origin private link location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfaf-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="2cfaf-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="2cfaf-138">Azure CDN Origin-Ressourcen-ID für private Links.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-138">Azure CDN origin private link resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfaf-139">-Profilname</span><span class="sxs-lookup"><span data-stu-id="2cfaf-139">-ProfileName</span></span>
<span data-ttu-id="2cfaf-140">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="2cfaf-140">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfaf-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cfaf-141">-ResourceGroupName</span></span>
<span data-ttu-id="2cfaf-142">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-142">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfaf-143">-Gewicht</span><span class="sxs-lookup"><span data-stu-id="2cfaf-143">-Weight</span></span>
<span data-ttu-id="2cfaf-144">Azure CDN-Ursprungs Gewicht.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-144">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfaf-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2cfaf-145">-Confirm</span></span>
<span data-ttu-id="2cfaf-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cfaf-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cfaf-147">-WhatIf</span></span>
<span data-ttu-id="2cfaf-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2cfaf-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cfaf-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfaf-150">CommonParameters</span></span>
<span data-ttu-id="2cfaf-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cfaf-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfaf-152">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cfaf-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfaf-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2cfaf-153">INPUTS</span></span>

### <span data-ttu-id="2cfaf-154">Keine</span><span class="sxs-lookup"><span data-stu-id="2cfaf-154">None</span></span>

## <span data-ttu-id="2cfaf-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2cfaf-155">OUTPUTS</span></span>

### <span data-ttu-id="2cfaf-156">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="2cfaf-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="2cfaf-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="2cfaf-157">NOTES</span></span>

## <span data-ttu-id="2cfaf-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2cfaf-158">RELATED LINKS</span></span>
