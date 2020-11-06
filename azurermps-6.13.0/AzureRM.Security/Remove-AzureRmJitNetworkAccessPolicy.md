---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 19de4ad776814efa55cdff19b2a77673d8581992
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482061"
---
# <span data-ttu-id="68e89-101">Remove-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68e89-101">Remove-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="68e89-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68e89-102">SYNOPSIS</span></span>
<span data-ttu-id="68e89-103">Löscht eine JIT-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="68e89-103">Deletes a JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68e89-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68e89-104">SYNTAX</span></span>

### <span data-ttu-id="68e89-105">ResourceGroupLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="68e89-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68e89-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="68e89-106">ResourceId</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68e89-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="68e89-107">InputObject</span></span>
```
Remove-AzureRmJitNetworkAccessPolicy -InputObject <PSRemoveJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68e89-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68e89-108">DESCRIPTION</span></span>
<span data-ttu-id="68e89-109">Löscht eine Just-in-Time-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="68e89-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="68e89-110">Nach dieser Aktion kann ein Benutzer keine temporäre Netzwerkverbindung auf den VMS anfordern, die innerhalb der gelöschten Richtlinie konfiguriert wurden.</span><span class="sxs-lookup"><span data-stu-id="68e89-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="68e89-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68e89-111">EXAMPLES</span></span>

### <span data-ttu-id="68e89-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="68e89-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="68e89-113">Löscht eine Just-in-Time-Netzwerkzugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="68e89-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="68e89-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="68e89-114">PARAMETERS</span></span>

### <span data-ttu-id="68e89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e89-115">-DefaultProfile</span></span>
<span data-ttu-id="68e89-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="68e89-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68e89-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="68e89-117">-InputObject</span></span>
<span data-ttu-id="68e89-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="68e89-118">Input Object.</span></span>

```yaml
Type: PSRemoveJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68e89-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="68e89-119">-Location</span></span>
<span data-ttu-id="68e89-120">Lage.</span><span class="sxs-lookup"><span data-stu-id="68e89-120">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e89-121">-Name</span><span class="sxs-lookup"><span data-stu-id="68e89-121">-Name</span></span>
<span data-ttu-id="68e89-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="68e89-122">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e89-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68e89-123">-PassThru</span></span>
<span data-ttu-id="68e89-124">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="68e89-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="68e89-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68e89-125">-ResourceGroupName</span></span>
<span data-ttu-id="68e89-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="68e89-126">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68e89-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="68e89-127">-ResourceId</span></span>
<span data-ttu-id="68e89-128">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="68e89-128">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68e89-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="68e89-129">-Confirm</span></span>
<span data-ttu-id="68e89-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="68e89-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68e89-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68e89-131">-WhatIf</span></span>
<span data-ttu-id="68e89-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="68e89-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68e89-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="68e89-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68e89-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e89-134">CommonParameters</span></span>
<span data-ttu-id="68e89-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68e89-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e89-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e89-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e89-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68e89-137">INPUTS</span></span>

### <span data-ttu-id="68e89-138">System. String</span><span class="sxs-lookup"><span data-stu-id="68e89-138">System.String</span></span>
<span data-ttu-id="68e89-139">Microsoft. Azure. Commands. Security. Cmdlets. JitNetworkAccessPolicies. PSRemoveJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68e89-139">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSRemoveJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="68e89-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68e89-140">OUTPUTS</span></span>

### <span data-ttu-id="68e89-141">Microsoft. Azure. Commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="68e89-141">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="68e89-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="68e89-142">NOTES</span></span>

## <span data-ttu-id="68e89-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68e89-143">RELATED LINKS</span></span>
