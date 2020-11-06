---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 4e252001d1459c52a35b766d34c91050df62073d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483110"
---
# <span data-ttu-id="51795-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="51795-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="51795-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51795-102">SYNOPSIS</span></span>
<span data-ttu-id="51795-103">Erstellt ein Configuration-Objekt für SQL Server Key Vault-Anmeldeinformationen auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="51795-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51795-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51795-104">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51795-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51795-105">DESCRIPTION</span></span>

## <span data-ttu-id="51795-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51795-106">EXAMPLES</span></span>

## <span data-ttu-id="51795-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="51795-107">PARAMETERS</span></span>

### <span data-ttu-id="51795-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="51795-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="51795-109">-Credentialname</span><span class="sxs-lookup"><span data-stu-id="51795-109">-CredentialName</span></span>
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

### <span data-ttu-id="51795-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="51795-110">-Enable</span></span>
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

### <span data-ttu-id="51795-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51795-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="51795-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="51795-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="51795-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="51795-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="51795-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="51795-114">-Confirm</span></span>
<span data-ttu-id="51795-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51795-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51795-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51795-116">-WhatIf</span></span>
<span data-ttu-id="51795-117">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51795-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="51795-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51795-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51795-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51795-119">CommonParameters</span></span>
<span data-ttu-id="51795-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51795-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51795-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51795-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51795-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51795-122">INPUTS</span></span>

### <span data-ttu-id="51795-123">Keine</span><span class="sxs-lookup"><span data-stu-id="51795-123">None</span></span>
<span data-ttu-id="51795-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="51795-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="51795-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51795-125">OUTPUTS</span></span>

## <span data-ttu-id="51795-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="51795-126">NOTES</span></span>

## <span data-ttu-id="51795-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51795-127">RELATED LINKS</span></span>

