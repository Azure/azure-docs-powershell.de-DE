---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: d9f732a40b61687d7970fdf24f9f9f0f841b2cc7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844460"
---
# <span data-ttu-id="ccd1a-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="ccd1a-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="ccd1a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ccd1a-102">SYNOPSIS</span></span>
<span data-ttu-id="ccd1a-103">Erstellt ein Configuration-Objekt für SQL Server Key Vault-Anmeldeinformationen auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="ccd1a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccd1a-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccd1a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ccd1a-105">DESCRIPTION</span></span>

## <span data-ttu-id="ccd1a-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ccd1a-106">EXAMPLES</span></span>

## <span data-ttu-id="ccd1a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccd1a-107">PARAMETERS</span></span>

### <span data-ttu-id="ccd1a-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="ccd1a-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="ccd1a-109">-Credentialname</span><span class="sxs-lookup"><span data-stu-id="ccd1a-109">-CredentialName</span></span>
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

### <span data-ttu-id="ccd1a-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="ccd1a-110">-Enable</span></span>
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

### <span data-ttu-id="ccd1a-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccd1a-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ccd1a-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="ccd1a-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="ccd1a-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="ccd1a-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="ccd1a-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ccd1a-114">-Confirm</span></span>
<span data-ttu-id="ccd1a-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccd1a-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccd1a-116">-WhatIf</span></span>
<span data-ttu-id="ccd1a-117">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ccd1a-118">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccd1a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccd1a-119">CommonParameters</span></span>
<span data-ttu-id="ccd1a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccd1a-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccd1a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccd1a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ccd1a-122">INPUTS</span></span>

### <span data-ttu-id="ccd1a-123">Keine</span><span class="sxs-lookup"><span data-stu-id="ccd1a-123">None</span></span>
<span data-ttu-id="ccd1a-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ccd1a-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ccd1a-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ccd1a-125">OUTPUTS</span></span>

### <span data-ttu-id="ccd1a-126">Microsoft. Azure. Commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="ccd1a-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="ccd1a-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="ccd1a-127">NOTES</span></span>

## <span data-ttu-id="ccd1a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ccd1a-128">RELATED LINKS</span></span>

