---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
ms.openlocfilehash: ee627065d1d6be8037d1a9b054ec6452b9becb41
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850123"
---
# <span data-ttu-id="7ee72-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="7ee72-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="7ee72-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ee72-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee72-103">Erstellt ein Configuration-Objekt für SQL Server Key Vault-Anmeldeinformationen auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="7ee72-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ee72-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ee72-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ee72-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ee72-105">DESCRIPTION</span></span>

## <span data-ttu-id="7ee72-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ee72-106">EXAMPLES</span></span>

## <span data-ttu-id="7ee72-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ee72-107">PARAMETERS</span></span>

### <span data-ttu-id="7ee72-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="7ee72-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee72-109">-Credentialname</span><span class="sxs-lookup"><span data-stu-id="7ee72-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee72-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="7ee72-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee72-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ee72-111">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee72-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="7ee72-112">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee72-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="7ee72-113">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ee72-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7ee72-114">-Confirm</span></span>
<span data-ttu-id="7ee72-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ee72-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ee72-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ee72-116">-WhatIf</span></span>
<span data-ttu-id="7ee72-117">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ee72-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7ee72-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ee72-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ee72-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee72-119">CommonParameters</span></span>
<span data-ttu-id="7ee72-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ee72-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee72-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ee72-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee72-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ee72-122">INPUTS</span></span>

### <span data-ttu-id="7ee72-123">Keine</span><span class="sxs-lookup"><span data-stu-id="7ee72-123">None</span></span>
<span data-ttu-id="7ee72-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7ee72-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7ee72-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ee72-125">OUTPUTS</span></span>

### <span data-ttu-id="7ee72-126">Microsoft. Azure. Commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="7ee72-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="7ee72-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ee72-127">NOTES</span></span>

## <span data-ttu-id="7ee72-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ee72-128">RELATED LINKS</span></span>

