---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/import-AzWebAppKeyVaultCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
ms.openlocfilehash: 61f498a521134ee0abb74f45ff048c94e7c53081
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157737"
---
# <span data-ttu-id="904da-101">Import-AzWebAppKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="904da-101">Import-AzWebAppKeyVaultCertificate</span></span>

## <span data-ttu-id="904da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="904da-102">SYNOPSIS</span></span>
<span data-ttu-id="904da-103">Importieren Sie ein ZERTIFIKAT aus dem Schlüsseltresor in eine Web App.</span><span class="sxs-lookup"><span data-stu-id="904da-103">Import an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="904da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="904da-104">SYNTAX</span></span>

```
Import-AzWebAppKeyVaultCertificate [-KeyVaultName] <String> [-CertName] <String> [-ResourceGroupName] <String>
 [-WebAppName] <String> [-Slot <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="904da-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="904da-105">DESCRIPTION</span></span>
<span data-ttu-id="904da-106">Das **Cmdlet "Import-AzWebAppKeyVaultCertificate"** importiert ein ZERTIFIKAT aus dem Schlüsseltresor in eine Web App.</span><span class="sxs-lookup"><span data-stu-id="904da-106">The **Import-AzWebAppKeyVaultCertificate** cmdlet imports an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="904da-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="904da-107">EXAMPLES</span></span>

### <span data-ttu-id="904da-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="904da-108">Example 1</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName "ContosoKeyVault" -CertName "ContosoCertname"
```

<span data-ttu-id="904da-109">Mit diesem Befehl wird ein -SSL-Zertifikat aus dem Schlüsseltresor in eine Web App importiert.</span><span class="sxs-lookup"><span data-stu-id="904da-109">This command imports an SSL certificate to a web app from Key Vault.</span></span>

### <span data-ttu-id="904da-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="904da-110">Example 2</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName  '/subscriptions/[sub id]/resourceGroups/[rg]/providers/Microsoft.KeyVault/vaults/[vault name]' 
-CertName "ContosoCertname"
```

<span data-ttu-id="904da-111">Mit diesem Befehl wird ein ZERTIFIKAT aus dem Schlüsseltresor mithilfe der Ressourcen-ID in eine Web App importiert (normalerweise, wenn sich der Schlüsseltresor in einem anderen Abonnement befindet).</span><span class="sxs-lookup"><span data-stu-id="904da-111">This command Import an SSL certificate to a web app from Key Vault using resource id (typically if Key Vault is in another subscription).</span></span>

## <span data-ttu-id="904da-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="904da-112">PARAMETERS</span></span>

### <span data-ttu-id="904da-113">-CertName</span><span class="sxs-lookup"><span data-stu-id="904da-113">-CertName</span></span>
<span data-ttu-id="904da-114">KeyVaultCertName des in keyvault erstellten Zertifikats</span><span class="sxs-lookup"><span data-stu-id="904da-114">KeyVaultCertName of the certificate created in keyvault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="904da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="904da-115">-DefaultProfile</span></span>
<span data-ttu-id="904da-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="904da-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="904da-117">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="904da-117">-KeyVaultName</span></span>
<span data-ttu-id="904da-118">Der Name des Keyvault.</span><span class="sxs-lookup"><span data-stu-id="904da-118">The name of the keyvault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="904da-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="904da-119">-ResourceGroupName</span></span>
<span data-ttu-id="904da-120">Der Name der WebApp-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="904da-120">The name of the webapp resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="904da-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="904da-121">-Slot</span></span>
<span data-ttu-id="904da-122">Der Name des Webapp-Slot.</span><span class="sxs-lookup"><span data-stu-id="904da-122">The name of the webapp slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="904da-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="904da-123">-WebAppName</span></span>
<span data-ttu-id="904da-124">Der Name der WebApp.</span><span class="sxs-lookup"><span data-stu-id="904da-124">The name of the webapp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="904da-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="904da-125">-Confirm</span></span>
<span data-ttu-id="904da-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="904da-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="904da-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="904da-127">-WhatIf</span></span>
<span data-ttu-id="904da-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="904da-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="904da-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="904da-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="904da-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="904da-130">CommonParameters</span></span>
<span data-ttu-id="904da-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="904da-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="904da-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="904da-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="904da-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="904da-133">INPUTS</span></span>

### <span data-ttu-id="904da-134">Keine</span><span class="sxs-lookup"><span data-stu-id="904da-134">None</span></span>

## <span data-ttu-id="904da-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="904da-135">OUTPUTS</span></span>

### <span data-ttu-id="904da-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="904da-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="904da-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="904da-137">NOTES</span></span>

## <span data-ttu-id="904da-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="904da-138">RELATED LINKS</span></span>
