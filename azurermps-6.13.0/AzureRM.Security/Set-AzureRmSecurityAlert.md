---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAlert.md
ms.openlocfilehash: 81cb94cdcb8efa948160d21da3aca709bb86b6fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482053"
---
# <span data-ttu-id="33525-101">Set-AzureRmSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="33525-101">Set-AzureRmSecurityAlert</span></span>

## <span data-ttu-id="33525-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="33525-102">SYNOPSIS</span></span>
<span data-ttu-id="33525-103">Aktualisiert einen Sicherheits Warnungszustand.</span><span class="sxs-lookup"><span data-stu-id="33525-103">Updates a security alert state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33525-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="33525-104">SYNTAX</span></span>

### <span data-ttu-id="33525-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="33525-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33525-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="33525-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33525-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="33525-107">ResourceId</span></span>
```
Set-AzureRmSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33525-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="33525-108">InputObject</span></span>
```
Set-AzureRmSecurityAlert [-ActionType <String>] -InputObject <PSSetAlertInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33525-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33525-109">DESCRIPTION</span></span>
<span data-ttu-id="33525-110">Legt einen Sicherheits Warnungsstatus fest.</span><span class="sxs-lookup"><span data-stu-id="33525-110">Sets a security alert state.</span></span>

## <span data-ttu-id="33525-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="33525-111">EXAMPLES</span></span>

### <span data-ttu-id="33525-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="33525-112">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="33525-113">Gibt eine ausgelöste Sicherheitswarnung aus.</span><span class="sxs-lookup"><span data-stu-id="33525-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="33525-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="33525-114">PARAMETERS</span></span>

### <span data-ttu-id="33525-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="33525-115">-ActionType</span></span>
<span data-ttu-id="33525-116">Aktionstyp</span><span class="sxs-lookup"><span data-stu-id="33525-116">Action Type.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33525-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33525-117">-DefaultProfile</span></span>
<span data-ttu-id="33525-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="33525-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33525-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="33525-119">-InputObject</span></span>
<span data-ttu-id="33525-120">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="33525-120">Input Object.</span></span>

```yaml
Type: PSSetAlertInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33525-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="33525-121">-Location</span></span>
<span data-ttu-id="33525-122">Lage.</span><span class="sxs-lookup"><span data-stu-id="33525-122">Location.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33525-123">-Name</span><span class="sxs-lookup"><span data-stu-id="33525-123">-Name</span></span>
<span data-ttu-id="33525-124">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="33525-124">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33525-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33525-125">-PassThru</span></span>
<span data-ttu-id="33525-126">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="33525-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="33525-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33525-127">-ResourceGroupName</span></span>
<span data-ttu-id="33525-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="33525-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33525-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="33525-129">-ResourceId</span></span>
<span data-ttu-id="33525-130">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="33525-130">Resource ID.</span></span>

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

### <span data-ttu-id="33525-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="33525-131">-Confirm</span></span>
<span data-ttu-id="33525-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="33525-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33525-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33525-133">-WhatIf</span></span>
<span data-ttu-id="33525-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="33525-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33525-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="33525-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33525-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33525-136">CommonParameters</span></span>
<span data-ttu-id="33525-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33525-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33525-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33525-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33525-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="33525-139">INPUTS</span></span>

### <span data-ttu-id="33525-140">System. String</span><span class="sxs-lookup"><span data-stu-id="33525-140">System.String</span></span>
<span data-ttu-id="33525-141">Microsoft. Azure. Commands. Security. Cmdlets. alerts. PSSetAlertInputObject</span><span class="sxs-lookup"><span data-stu-id="33525-141">Microsoft.Azure.Commands.Security.Cmdlets.Alerts.PSSetAlertInputObject</span></span>

## <span data-ttu-id="33525-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="33525-142">OUTPUTS</span></span>

### <span data-ttu-id="33525-143">Microsoft. Azure. Commands. Security. Models. alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="33525-143">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="33525-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="33525-144">NOTES</span></span>

## <span data-ttu-id="33525-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="33525-145">RELATED LINKS</span></span>
