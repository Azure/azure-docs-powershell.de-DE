---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: 8198d189d9619528bdc7fb80d30285ce9126dfed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179302"
---
# <span data-ttu-id="2d23e-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2d23e-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="2d23e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d23e-102">SYNOPSIS</span></span>
<span data-ttu-id="2d23e-103">Entfernt einen CDN-Ursprung</span><span class="sxs-lookup"><span data-stu-id="2d23e-103">Removes a CDN origin</span></span>

## <span data-ttu-id="2d23e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d23e-104">SYNTAX</span></span>

### <span data-ttu-id="2d23e-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d23e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d23e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d23e-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d23e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d23e-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d23e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d23e-108">DESCRIPTION</span></span>
<span data-ttu-id="2d23e-109">Remove-AzCdnOrigin löscht einen CDN-Ursprung aus dem angegebenen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="2d23e-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="2d23e-110">Wenn der Ursprung der einzige Ursprung innerhalb des angegebenen Endpunkts ist, schlägt der Löschvorgang fehl, da mindestens 1 Ursprung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="2d23e-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="2d23e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d23e-111">EXAMPLES</span></span>

### <span data-ttu-id="2d23e-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2d23e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="2d23e-113">Mit diesem Cmdlet wird der angegebene Ursprung vom angegebenen Endpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="2d23e-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="2d23e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d23e-114">PARAMETERS</span></span>

### <span data-ttu-id="2d23e-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2d23e-115">-CdnOrigin</span></span>
<span data-ttu-id="2d23e-116">Das CDN-Ursprungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="2d23e-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="2d23e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d23e-117">-DefaultProfile</span></span>
<span data-ttu-id="2d23e-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2d23e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d23e-119">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="2d23e-119">-EndpointName</span></span>
<span data-ttu-id="2d23e-120">Azure CDN-Endpunktname.</span><span class="sxs-lookup"><span data-stu-id="2d23e-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="2d23e-121">-OriginName</span><span class="sxs-lookup"><span data-stu-id="2d23e-121">-OriginName</span></span>
<span data-ttu-id="2d23e-122">Azure CDN-Ursprungsname.</span><span class="sxs-lookup"><span data-stu-id="2d23e-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="2d23e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d23e-123">-PassThru</span></span>
<span data-ttu-id="2d23e-124">Gibt das Objekt zurück, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="2d23e-124">Return object if specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d23e-125">-Profilname</span><span class="sxs-lookup"><span data-stu-id="2d23e-125">-ProfileName</span></span>
<span data-ttu-id="2d23e-126">Azure CDN-Profilname</span><span class="sxs-lookup"><span data-stu-id="2d23e-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="2d23e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d23e-127">-ResourceGroupName</span></span>
<span data-ttu-id="2d23e-128">Die Ressourcengruppe des Azure CDN-Profils.</span><span class="sxs-lookup"><span data-stu-id="2d23e-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="2d23e-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2d23e-129">-ResourceId</span></span>
<span data-ttu-id="2d23e-130">Die Ressourcen-ID des Azure CDN-Ursprungs.</span><span class="sxs-lookup"><span data-stu-id="2d23e-130">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d23e-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d23e-131">-Confirm</span></span>
<span data-ttu-id="2d23e-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d23e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d23e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d23e-133">-WhatIf</span></span>
<span data-ttu-id="2d23e-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d23e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d23e-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d23e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d23e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d23e-136">CommonParameters</span></span>
<span data-ttu-id="2d23e-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d23e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d23e-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d23e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d23e-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d23e-139">INPUTS</span></span>

### <span data-ttu-id="2d23e-140">Keine</span><span class="sxs-lookup"><span data-stu-id="2d23e-140">None</span></span>

## <span data-ttu-id="2d23e-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d23e-141">OUTPUTS</span></span>

### <span data-ttu-id="2d23e-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2d23e-142">System.Boolean</span></span>

## <span data-ttu-id="2d23e-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d23e-143">NOTES</span></span>

## <span data-ttu-id="2d23e-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d23e-144">RELATED LINKS</span></span>
