---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: 102f1ebc6152bb521bd1f9c7214a6c48ee61a274
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950531"
---
# <span data-ttu-id="a7f6b-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="a7f6b-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="a7f6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7f6b-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f6b-103">Widerrufen Sie alle Benutzerdelegierungsschlüssel eines Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="a7f6b-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="a7f6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7f6b-104">SYNTAX</span></span>

### <span data-ttu-id="a7f6b-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7f6b-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7f6b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a7f6b-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7f6b-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="a7f6b-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7f6b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7f6b-108">DESCRIPTION</span></span>
<span data-ttu-id="a7f6b-109">Das **Cmdlet Revoke-AzStorageAccountUserDelegationKeys** widerruft alle Benutzerdelegierungsschlüssel eines Speicherkontos, sodass auch alle Identity SAS-Token des Speicherkontos widerrufen werden.</span><span class="sxs-lookup"><span data-stu-id="a7f6b-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="a7f6b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a7f6b-110">EXAMPLES</span></span>

### <span data-ttu-id="a7f6b-111">Beispiel 1: Widerrufen aller Benutzerdelegierungsschlüssel eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="a7f6b-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="a7f6b-112">In diesem Beispiel werden alle Benutzerdelegierungsschlüssel eines Speicherkontos widerrufen, sodass auch das von den Benutzerdelegierungsschlüsseln generierte Identity SAS-Token widerrufen wird.</span><span class="sxs-lookup"><span data-stu-id="a7f6b-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="a7f6b-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a7f6b-113">PARAMETERS</span></span>

### <span data-ttu-id="a7f6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7f6b-114">-DefaultProfile</span></span>
<span data-ttu-id="a7f6b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7f6b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7f6b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7f6b-116">-InputObject</span></span>
<span data-ttu-id="a7f6b-117">Ein Speicherkontoobjekt, das von Get_AzStorageAccount, New-AzStorageAccount, zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a7f6b-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f6b-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7f6b-118">-PassThru</span></span>
<span data-ttu-id="a7f6b-119">Normalerweise gibt dieses Cmdlet bei erfolgreichem Abschluss keine Ausgabe zurück. Dieser Parameter zwingt das Cmdlet, bei erfolgreichem Abschluss einen Wert ($true) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a7f6b-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="a7f6b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f6b-120">-ResourceGroupName</span></span>
<span data-ttu-id="a7f6b-121">Der Name der Ressourcengruppe, der die Speicherkontoressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a7f6b-121">The resource group name containing the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f6b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7f6b-122">-ResourceId</span></span>
<span data-ttu-id="a7f6b-123">Ressourcen-ID des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="a7f6b-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases: StorageAccountResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f6b-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a7f6b-124">-StorageAccountName</span></span>
<span data-ttu-id="a7f6b-125">Der Name der Speicherkontoressource.</span><span class="sxs-lookup"><span data-stu-id="a7f6b-125">The name of the storage account resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f6b-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7f6b-126">-Confirm</span></span>
<span data-ttu-id="a7f6b-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7f6b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7f6b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f6b-128">-WhatIf</span></span>
<span data-ttu-id="a7f6b-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7f6b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7f6b-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7f6b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7f6b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7f6b-131">CommonParameters</span></span>
<span data-ttu-id="a7f6b-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7f6b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7f6b-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7f6b-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7f6b-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a7f6b-134">INPUTS</span></span>

### <span data-ttu-id="a7f6b-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a7f6b-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a7f6b-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a7f6b-136">System.String</span></span>

## <span data-ttu-id="a7f6b-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a7f6b-137">OUTPUTS</span></span>

### <span data-ttu-id="a7f6b-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a7f6b-138">System.Boolean</span></span>

## <span data-ttu-id="a7f6b-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a7f6b-139">NOTES</span></span>

## <span data-ttu-id="a7f6b-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a7f6b-140">RELATED LINKS</span></span>
