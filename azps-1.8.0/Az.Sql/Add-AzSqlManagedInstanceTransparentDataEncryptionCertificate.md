---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate.md
ms.openlocfilehash: dc73939aaae76c0444307cbd1aa6bfb08711b2e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659289"
---
# <span data-ttu-id="42419-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="42419-101">Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

## <span data-ttu-id="42419-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42419-102">SYNOPSIS</span></span>
<span data-ttu-id="42419-103">Hinzufügen eines transparenten Daten Verschlüsselungszertifikats für die angegebene verwaltete Instanz</span><span class="sxs-lookup"><span data-stu-id="42419-103">Adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="42419-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42419-104">SYNTAX</span></span>

```
Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate [-PassThru] [-ResourceGroupName] <String>
 [-ManagedInstanceName] <String> [-PrivateBlob] <SecureString> [-Password] <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42419-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42419-105">DESCRIPTION</span></span>
<span data-ttu-id="42419-106">Das Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate fügt ein transparentes Daten Verschlüsselungszertifikat für die angegebene verwaltete Instanz hinzu.</span><span class="sxs-lookup"><span data-stu-id="42419-106">The Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate adds a Transparent Data Encryption Certificate for the given managed instance</span></span>

## <span data-ttu-id="42419-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42419-107">EXAMPLES</span></span>

### <span data-ttu-id="42419-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="42419-108">Example 1</span></span>
```powershell
PS C:\>     $privateBlob = "MIIJ+QIBAzCCCbUGCSqGSIb3DQEHAaCCCaYEggmiMIIJnjCCBhcGCSqGSIb3Dasdsadasd"
PS C:\>     $securePrivateBlob = $privateBlob  | ConvertTo-SecureString -AsPlainText -Force
PS C:\>     $password = "CertificatePassword"
PS C:\>     $securePassword = $password | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Add-AzSqlManagedInstanceTransparentDataEncryptionCertificate -ResourceGroupName "YourResourceGroupName" -ManagedInstanceName "YourManagedInstanceName" -PrivateBlob $securePrivateBlob -Password $securePassword
```

## <span data-ttu-id="42419-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="42419-109">PARAMETERS</span></span>

### <span data-ttu-id="42419-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42419-110">-DefaultProfile</span></span>
<span data-ttu-id="42419-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42419-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42419-112">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="42419-112">-ManagedInstanceName</span></span>
<span data-ttu-id="42419-113">Name der verwalteten Instanz</span><span class="sxs-lookup"><span data-stu-id="42419-113">The managed instance name</span></span>

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

### <span data-ttu-id="42419-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42419-114">-PassThru</span></span>
<span data-ttu-id="42419-115">Bei erfolgreicher Ausführung gibt Certificate-Objekt zurück, das hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="42419-115">On Successful execution, returns certificate object that was added.</span></span>

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

### <span data-ttu-id="42419-116">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="42419-116">-Password</span></span>
<span data-ttu-id="42419-117">Das Kennwort für das transparente Daten Verschlüsselungszertifikat</span><span class="sxs-lookup"><span data-stu-id="42419-117">The Password for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42419-118">-PrivateBlob</span><span class="sxs-lookup"><span data-stu-id="42419-118">-PrivateBlob</span></span>
<span data-ttu-id="42419-119">Das private BLOB für das transparente Daten Verschlüsselungszertifikat</span><span class="sxs-lookup"><span data-stu-id="42419-119">The Private blob for Transparent Data Encryption Certificate</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42419-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42419-120">-ResourceGroupName</span></span>
<span data-ttu-id="42419-121">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="42419-121">The Resource Group Name</span></span>

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

### <span data-ttu-id="42419-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="42419-122">-Confirm</span></span>
<span data-ttu-id="42419-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42419-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42419-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42419-124">-WhatIf</span></span>
<span data-ttu-id="42419-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42419-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42419-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42419-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42419-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42419-127">CommonParameters</span></span>
<span data-ttu-id="42419-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42419-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42419-129">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42419-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42419-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42419-130">INPUTS</span></span>

### <span data-ttu-id="42419-131">Keine</span><span class="sxs-lookup"><span data-stu-id="42419-131">None</span></span>

## <span data-ttu-id="42419-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42419-132">OUTPUTS</span></span>

### <span data-ttu-id="42419-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="42419-133">System.Boolean</span></span>

## <span data-ttu-id="42419-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="42419-134">NOTES</span></span>

## <span data-ttu-id="42419-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42419-135">RELATED LINKS</span></span>
