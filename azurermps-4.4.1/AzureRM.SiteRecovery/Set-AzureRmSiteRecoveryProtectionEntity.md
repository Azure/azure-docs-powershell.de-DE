---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 245eb56ea973c1330b7f8b9d32a3f0b9584bd0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663515"
---
# <span data-ttu-id="c78a3-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c78a3-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="c78a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c78a3-102">SYNOPSIS</span></span>
<span data-ttu-id="c78a3-103">Legt den Zustand für eine Website Wiederherstellungs Schutz Entität fest.</span><span class="sxs-lookup"><span data-stu-id="c78a3-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c78a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c78a3-104">SYNTAX</span></span>

### <span data-ttu-id="c78a3-105">Disabled (Standard)</span><span class="sxs-lookup"><span data-stu-id="c78a3-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c78a3-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="c78a3-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c78a3-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="c78a3-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c78a3-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="c78a3-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c78a3-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c78a3-109">DESCRIPTION</span></span>
<span data-ttu-id="c78a3-110">Das Cmdlet " **Satz-AzureRmSiteRecoveryProtectionEntity** " aktiviert oder deaktiviert den Schutz für eine Azure Site Recovery Protection-Entität.</span><span class="sxs-lookup"><span data-stu-id="c78a3-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="c78a3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c78a3-111">EXAMPLES</span></span>

## <span data-ttu-id="c78a3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c78a3-112">PARAMETERS</span></span>

### <span data-ttu-id="c78a3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c78a3-113">-Force</span></span>
<span data-ttu-id="c78a3-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c78a3-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c78a3-115">-OS</span><span class="sxs-lookup"><span data-stu-id="c78a3-115">-OS</span></span>
<span data-ttu-id="c78a3-116">Gibt den Typ des Betriebssystems an.</span><span class="sxs-lookup"><span data-stu-id="c78a3-116">Specifies the operating system type.</span></span>
<span data-ttu-id="c78a3-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c78a3-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c78a3-118">Windows</span><span class="sxs-lookup"><span data-stu-id="c78a3-118">Windows</span></span>
- <span data-ttu-id="c78a3-119">Linux</span><span class="sxs-lookup"><span data-stu-id="c78a3-119">Linux</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78a3-120">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="c78a3-120">-OSDiskName</span></span>
<span data-ttu-id="c78a3-121">Gibt den Namen des Datenträgers an, der das Betriebssystem enthält.</span><span class="sxs-lookup"><span data-stu-id="c78a3-121">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78a3-122">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="c78a3-122">-Policy</span></span>
<span data-ttu-id="c78a3-123">Gibt das Website Wiederherstellungsrichtlinien Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c78a3-123">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78a3-124">-Schutz</span><span class="sxs-lookup"><span data-stu-id="c78a3-124">-Protection</span></span>
<span data-ttu-id="c78a3-125">Gibt an, ob der Schutz aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c78a3-125">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="c78a3-126">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c78a3-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c78a3-127">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="c78a3-127">Enable</span></span>
- <span data-ttu-id="c78a3-128">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="c78a3-128">Disable</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78a3-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c78a3-129">-ProtectionEntity</span></span>
<span data-ttu-id="c78a3-130">Gibt das Schutz Entitätsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="c78a3-130">Specifies the protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c78a3-131">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c78a3-131">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="c78a3-132">Gibt die ID des Ziel-Azure-speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="c78a3-132">Specifies the ID of the target Azure Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c78a3-133">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="c78a3-133">-WaitForCompletion</span></span>
<span data-ttu-id="c78a3-134">Gibt an, dass der Befehl vor der Rückgabe auf Abschluss wartet.</span><span class="sxs-lookup"><span data-stu-id="c78a3-134">Indicates that the command waits for completion before returning.</span></span>

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

### <span data-ttu-id="c78a3-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c78a3-135">-Confirm</span></span>
<span data-ttu-id="c78a3-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c78a3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c78a3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c78a3-137">-WhatIf</span></span>
<span data-ttu-id="c78a3-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c78a3-138">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c78a3-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c78a3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c78a3-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c78a3-140">-DefaultProfile</span></span>
<span data-ttu-id="c78a3-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c78a3-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c78a3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c78a3-142">CommonParameters</span></span>
<span data-ttu-id="c78a3-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c78a3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c78a3-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c78a3-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c78a3-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c78a3-145">INPUTS</span></span>

### <span data-ttu-id="c78a3-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c78a3-146">ASRProtectionEntity</span></span>
<span data-ttu-id="c78a3-147">Der Parameter "ProtectionEntity" akzeptiert den Wert vom Typ "ASRProtectionEntity" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="c78a3-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="c78a3-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c78a3-148">OUTPUTS</span></span>

### <span data-ttu-id="c78a3-149">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c78a3-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c78a3-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="c78a3-150">NOTES</span></span>

## <span data-ttu-id="c78a3-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c78a3-151">RELATED LINKS</span></span>

[<span data-ttu-id="c78a3-152">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="c78a3-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
