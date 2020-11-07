---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryprotectionentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 21bf19ba4a4d17ef41f6741deedd5cac486bbb32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662716"
---
# <span data-ttu-id="824aa-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="824aa-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="824aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="824aa-102">SYNOPSIS</span></span>
<span data-ttu-id="824aa-103">Legt den Zustand für eine Website Wiederherstellungs Schutz Entität fest.</span><span class="sxs-lookup"><span data-stu-id="824aa-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="824aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="824aa-104">SYNTAX</span></span>

### <span data-ttu-id="824aa-105">Disabled (Standard)</span><span class="sxs-lookup"><span data-stu-id="824aa-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="824aa-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="824aa-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="824aa-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="824aa-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="824aa-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="824aa-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="824aa-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="824aa-109">DESCRIPTION</span></span>
<span data-ttu-id="824aa-110">Das Cmdlet " **Satz-AzureRmSiteRecoveryProtectionEntity** " aktiviert oder deaktiviert den Schutz für eine Azure Site Recovery Protection-Entität.</span><span class="sxs-lookup"><span data-stu-id="824aa-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="824aa-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="824aa-111">EXAMPLES</span></span>

## <span data-ttu-id="824aa-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="824aa-112">PARAMETERS</span></span>

### <span data-ttu-id="824aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824aa-113">-DefaultProfile</span></span>
<span data-ttu-id="824aa-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="824aa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="824aa-115">-Force</span><span class="sxs-lookup"><span data-stu-id="824aa-115">-Force</span></span>
<span data-ttu-id="824aa-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="824aa-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="824aa-117">-OS</span><span class="sxs-lookup"><span data-stu-id="824aa-117">-OS</span></span>
<span data-ttu-id="824aa-118">Gibt den Typ des Betriebssystems an.</span><span class="sxs-lookup"><span data-stu-id="824aa-118">Specifies the operating system type.</span></span>
<span data-ttu-id="824aa-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="824aa-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="824aa-120">Windows</span><span class="sxs-lookup"><span data-stu-id="824aa-120">Windows</span></span>
- <span data-ttu-id="824aa-121">Linux</span><span class="sxs-lookup"><span data-stu-id="824aa-121">Linux</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824aa-122">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="824aa-122">-OSDiskName</span></span>
<span data-ttu-id="824aa-123">Gibt den Namen des Datenträgers an, der das Betriebssystem enthält.</span><span class="sxs-lookup"><span data-stu-id="824aa-123">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824aa-124">– Richtlinien</span><span class="sxs-lookup"><span data-stu-id="824aa-124">-Policy</span></span>
<span data-ttu-id="824aa-125">Gibt das Website Wiederherstellungsrichtlinien Objekt an.</span><span class="sxs-lookup"><span data-stu-id="824aa-125">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824aa-126">-Schutz</span><span class="sxs-lookup"><span data-stu-id="824aa-126">-Protection</span></span>
<span data-ttu-id="824aa-127">Gibt an, ob der Schutz aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="824aa-127">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="824aa-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="824aa-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="824aa-129">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="824aa-129">Enable</span></span>
- <span data-ttu-id="824aa-130">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="824aa-130">Disable</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824aa-131">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="824aa-131">-ProtectionEntity</span></span>
<span data-ttu-id="824aa-132">Gibt das Schutz Entitätsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="824aa-132">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="824aa-133">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="824aa-133">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="824aa-134">Gibt die ID des Ziel-Azure-speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="824aa-134">Specifies the ID of the target Azure Storage account.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824aa-135">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="824aa-135">-WaitForCompletion</span></span>
<span data-ttu-id="824aa-136">Gibt an, dass der Befehl vor der Rückgabe auf Abschluss wartet.</span><span class="sxs-lookup"><span data-stu-id="824aa-136">Indicates that the command waits for completion before returning.</span></span>

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

### <span data-ttu-id="824aa-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="824aa-137">-Confirm</span></span>
<span data-ttu-id="824aa-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="824aa-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824aa-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="824aa-139">-WhatIf</span></span>
<span data-ttu-id="824aa-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="824aa-140">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="824aa-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="824aa-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824aa-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824aa-142">CommonParameters</span></span>
<span data-ttu-id="824aa-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="824aa-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824aa-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="824aa-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824aa-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="824aa-145">INPUTS</span></span>

### <span data-ttu-id="824aa-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="824aa-146">ASRProtectionEntity</span></span>
<span data-ttu-id="824aa-147">Der Parameter "ProtectionEntity" akzeptiert den Wert vom Typ "ASRProtectionEntity" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="824aa-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="824aa-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="824aa-148">OUTPUTS</span></span>

### <span data-ttu-id="824aa-149">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="824aa-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="824aa-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="824aa-150">NOTES</span></span>

## <span data-ttu-id="824aa-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="824aa-151">RELATED LINKS</span></span>

[<span data-ttu-id="824aa-152">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="824aa-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
