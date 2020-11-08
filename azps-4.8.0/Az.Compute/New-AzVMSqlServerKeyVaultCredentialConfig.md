---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 50bf29524e4c16a7a7186a547505f4dcf7dac4e2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008615"
---
# <span data-ttu-id="218c3-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="218c3-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="218c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="218c3-102">SYNOPSIS</span></span>
<span data-ttu-id="218c3-103">Erstellt ein Configuration-Objekt für SQL Server Key Vault-Anmeldeinformationen auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="218c3-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="218c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="218c3-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="218c3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="218c3-105">DESCRIPTION</span></span>

## <span data-ttu-id="218c3-106">Beispiele</span><span class="sxs-lookup"><span data-stu-id="218c3-106">EXAMPLES</span></span>

## <span data-ttu-id="218c3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="218c3-107">PARAMETERS</span></span>

### <span data-ttu-id="218c3-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="218c3-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="218c3-109">Azure Key Vault-Dienst-URL</span><span class="sxs-lookup"><span data-stu-id="218c3-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="218c3-110">-Credentialname</span><span class="sxs-lookup"><span data-stu-id="218c3-110">-CredentialName</span></span>
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

### <span data-ttu-id="218c3-111">-Enable</span><span class="sxs-lookup"><span data-stu-id="218c3-111">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="218c3-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="218c3-112">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="218c3-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="218c3-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="218c3-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="218c3-114">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="218c3-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="218c3-115">-Confirm</span></span>
<span data-ttu-id="218c3-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="218c3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="218c3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="218c3-117">-WhatIf</span></span>
<span data-ttu-id="218c3-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="218c3-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="218c3-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="218c3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="218c3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="218c3-120">CommonParameters</span></span>
<span data-ttu-id="218c3-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="218c3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="218c3-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="218c3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="218c3-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="218c3-123">INPUTS</span></span>

### <span data-ttu-id="218c3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="218c3-124">System.String</span></span>

### <span data-ttu-id="218c3-125">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="218c3-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="218c3-126">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="218c3-126">System.Security.SecureString</span></span>

## <span data-ttu-id="218c3-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="218c3-127">OUTPUTS</span></span>

### <span data-ttu-id="218c3-128">Microsoft. Azure. Commands. Compute. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="218c3-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="218c3-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="218c3-129">NOTES</span></span>

## <span data-ttu-id="218c3-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="218c3-130">RELATED LINKS</span></span>
