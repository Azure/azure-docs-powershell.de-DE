---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 4b7719a43535de4af595e634dea2061ab9cba19d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172152"
---
# <span data-ttu-id="cc943-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cc943-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="cc943-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc943-102">SYNOPSIS</span></span>
<span data-ttu-id="cc943-103">Entfernt einen Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="cc943-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="cc943-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc943-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc943-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc943-105">DESCRIPTION</span></span>
<span data-ttu-id="cc943-106">Das **Cmdlet "Remove-AzRedisCache"** entfernt einen Azure Redis-Cache.</span><span class="sxs-lookup"><span data-stu-id="cc943-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="cc943-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cc943-107">EXAMPLES</span></span>

### <span data-ttu-id="cc943-108">Beispiel 1: Entfernen eines Caches für Redis und Zurückgeben des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="cc943-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="cc943-109">Dieser Befehl entfernt einen Redis-Cache und zeigt an, ob der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="cc943-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="cc943-110">Beispiel 2: Entfernen eines Caches für Redis und Nichtanzeige des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="cc943-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="cc943-111">Mit diesem Befehl wird ein Cache für Redis entfernt.</span><span class="sxs-lookup"><span data-stu-id="cc943-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="cc943-112">Da der *Parameter "PassThru"* nicht angegeben wird, wird das Ergebnis des Vorgangs nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cc943-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="cc943-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc943-113">PARAMETERS</span></span>

### <span data-ttu-id="cc943-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc943-114">-DefaultProfile</span></span>
<span data-ttu-id="cc943-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc943-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc943-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cc943-116">-Force</span></span>
<span data-ttu-id="cc943-117">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="cc943-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc943-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cc943-118">-Name</span></span>
<span data-ttu-id="cc943-119">Gibt den Namen des zu entfernenden Caches für Redis an.</span><span class="sxs-lookup"><span data-stu-id="cc943-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="cc943-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc943-120">-PassThru</span></span>
<span data-ttu-id="cc943-121">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cc943-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cc943-122">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="cc943-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cc943-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc943-123">-ResourceGroupName</span></span>
<span data-ttu-id="cc943-124">Gibt den Namen der Ressourcengruppe an, die den zu entfernenden Cache von Redis enthält.</span><span class="sxs-lookup"><span data-stu-id="cc943-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc943-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc943-125">-Confirm</span></span>
<span data-ttu-id="cc943-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc943-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc943-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cc943-127">-WhatIf</span></span>
<span data-ttu-id="cc943-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc943-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc943-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc943-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc943-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc943-130">CommonParameters</span></span>
<span data-ttu-id="cc943-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc943-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc943-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc943-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc943-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cc943-133">INPUTS</span></span>

### <span data-ttu-id="cc943-134">System.String</span><span class="sxs-lookup"><span data-stu-id="cc943-134">System.String</span></span>

## <span data-ttu-id="cc943-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cc943-135">OUTPUTS</span></span>

### <span data-ttu-id="cc943-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cc943-136">System.Boolean</span></span>

## <span data-ttu-id="cc943-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cc943-137">NOTES</span></span>

## <span data-ttu-id="cc943-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cc943-138">RELATED LINKS</span></span>

[<span data-ttu-id="cc943-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cc943-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="cc943-140">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cc943-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="cc943-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="cc943-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


