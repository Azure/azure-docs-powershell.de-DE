---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156092"
---
# <span data-ttu-id="1d3ad-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="1d3ad-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="1d3ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d3ad-102">SYNOPSIS</span></span>
<span data-ttu-id="1d3ad-103">Widerrufen sie alle Benutzerdelegierungsschlüssel eines Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="1d3ad-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="1d3ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d3ad-104">SYNTAX</span></span>

### <span data-ttu-id="1d3ad-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1d3ad-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d3ad-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1d3ad-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d3ad-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="1d3ad-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d3ad-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d3ad-108">DESCRIPTION</span></span>
<span data-ttu-id="1d3ad-109">Das **Cmdlet Revoke-AzStorageAccountUserDelegationKeys** widerruft alle Benutzerdelegierungsschlüssel eines Speicherkontos, sodass auch alle Identitäts-SAS-Token des Speicherkontos widerrufen werden.</span><span class="sxs-lookup"><span data-stu-id="1d3ad-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="1d3ad-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d3ad-110">EXAMPLES</span></span>

### <span data-ttu-id="1d3ad-111">Beispiel 1: Widerrufen aller Benutzerdelegierungsschlüssel eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="1d3ad-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="1d3ad-112">In diesem Beispiel werden alle Benutzerdelegierungsschlüssel eines Speicherkontos widerrufen, sodass auch alle von den Benutzerdelegierungsschlüsseln generierten Identitäts-SAS-Token widerrufen werden.</span><span class="sxs-lookup"><span data-stu-id="1d3ad-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="1d3ad-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d3ad-113">PARAMETERS</span></span>

### <span data-ttu-id="1d3ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d3ad-114">-DefaultProfile</span></span>
<span data-ttu-id="1d3ad-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d3ad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d3ad-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d3ad-116">-InputObject</span></span>
<span data-ttu-id="1d3ad-117">Ein Speicherkontoobjekt, das von Get_AzStorageAccount, New-AzStorageAccount, zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1d3ad-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

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

### <span data-ttu-id="1d3ad-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d3ad-118">-PassThru</span></span>
<span data-ttu-id="1d3ad-119">Normalerweise gibt dieses Cmdlet nach erfolgreichem Abschluss keine Ausgabe zurück. Dieser Parameter zwingt das Cmdlet, bei erfolgreichem Abschluss einen Wert ($true) zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="1d3ad-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="1d3ad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d3ad-120">-ResourceGroupName</span></span>
<span data-ttu-id="1d3ad-121">Der Name der Ressourcengruppe, der die Speicherkontoressource enthält.</span><span class="sxs-lookup"><span data-stu-id="1d3ad-121">The resource group name containing the storage account resource.</span></span>

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

### <span data-ttu-id="1d3ad-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d3ad-122">-ResourceId</span></span>
<span data-ttu-id="1d3ad-123">Ressourcen-ID des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="1d3ad-123">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="1d3ad-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1d3ad-124">-StorageAccountName</span></span>
<span data-ttu-id="1d3ad-125">Der Name der Speicherkontoressource.</span><span class="sxs-lookup"><span data-stu-id="1d3ad-125">The name of the storage account resource.</span></span>

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

### <span data-ttu-id="1d3ad-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d3ad-126">-Confirm</span></span>
<span data-ttu-id="1d3ad-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d3ad-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d3ad-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1d3ad-128">-WhatIf</span></span>
<span data-ttu-id="1d3ad-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d3ad-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d3ad-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d3ad-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d3ad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d3ad-131">CommonParameters</span></span>
<span data-ttu-id="1d3ad-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d3ad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d3ad-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d3ad-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d3ad-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d3ad-134">INPUTS</span></span>

### <span data-ttu-id="1d3ad-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d3ad-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="1d3ad-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1d3ad-136">System.String</span></span>

## <span data-ttu-id="1d3ad-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d3ad-137">OUTPUTS</span></span>

### <span data-ttu-id="1d3ad-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1d3ad-138">System.Boolean</span></span>

## <span data-ttu-id="1d3ad-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1d3ad-139">NOTES</span></span>

## <span data-ttu-id="1d3ad-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1d3ad-140">RELATED LINKS</span></span>
