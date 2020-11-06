---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
ms.openlocfilehash: a05662917d7e29f090867b0c91503292a9bc917e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477985"
---
# <span data-ttu-id="71c07-101">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="71c07-101">Set-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="71c07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71c07-102">SYNOPSIS</span></span>
<span data-ttu-id="71c07-103">Ändert eine Automatisierungs Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="71c07-103">Modifies an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71c07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71c07-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71c07-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71c07-105">DESCRIPTION</span></span>
<span data-ttu-id="71c07-106">Das Cmdlet " **Satz-AzureRmAutomationCredential** " ändert eine Anmeldeinformationen als **PSCredential** -Objekt in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="71c07-106">The **Set-AzureRmAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="71c07-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71c07-107">EXAMPLES</span></span>

### <span data-ttu-id="71c07-108">Beispiel 1: Aktualisieren von Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="71c07-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="71c07-109">Der erste Befehl weist der $User-Variablen einen Benutzernamen zu.</span><span class="sxs-lookup"><span data-stu-id="71c07-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="71c07-110">Mit dem zweiten Befehl wird ein nur-Text-Kennwort mithilfe des ConvertTo-SecureString-Cmdlets in eine sichere Zeichenfolge konvertiert.</span><span class="sxs-lookup"><span data-stu-id="71c07-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="71c07-111">Der Befehl speichert das Objekt in der $Password Variablen.</span><span class="sxs-lookup"><span data-stu-id="71c07-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="71c07-112">Der dritte Befehl erstellt eine Anmeldeinformationen basierend auf $User und $Password und speichert Sie dann in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="71c07-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="71c07-113">Der endgültige Befehl ändert die Automatisierungs Anmeldeinformationen mit dem Namen ContosoCredential, um die Anmeldeinformationen in $Credential zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="71c07-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="71c07-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="71c07-114">PARAMETERS</span></span>

### <span data-ttu-id="71c07-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="71c07-115">-AutomationAccountName</span></span>
<span data-ttu-id="71c07-116">Gibt den Namen des Automatisierungs Kontos an, für das mit diesem Cmdlet eine Anmeldeinformation geändert wird.</span><span class="sxs-lookup"><span data-stu-id="71c07-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c07-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71c07-117">-DefaultProfile</span></span>
<span data-ttu-id="71c07-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="71c07-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71c07-119">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71c07-119">-Description</span></span>
<span data-ttu-id="71c07-120">Gibt eine Beschreibung für die Anmeldeinformationen an, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="71c07-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="71c07-121">-Name</span><span class="sxs-lookup"><span data-stu-id="71c07-121">-Name</span></span>
<span data-ttu-id="71c07-122">Gibt den Namen der Anmeldeinformationen an, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="71c07-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c07-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71c07-123">-ResourceGroupName</span></span>
<span data-ttu-id="71c07-124">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine Anmeldeinformationen ändert.</span><span class="sxs-lookup"><span data-stu-id="71c07-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="71c07-125">-Wert</span><span class="sxs-lookup"><span data-stu-id="71c07-125">-Value</span></span>
<span data-ttu-id="71c07-126">Gibt die Anmeldeinformationen als **PSCredential** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="71c07-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71c07-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c07-127">CommonParameters</span></span>
<span data-ttu-id="71c07-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71c07-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c07-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c07-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c07-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71c07-130">INPUTS</span></span>

### <span data-ttu-id="71c07-131">System. String</span><span class="sxs-lookup"><span data-stu-id="71c07-131">System.String</span></span>

### <span data-ttu-id="71c07-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="71c07-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="71c07-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71c07-133">OUTPUTS</span></span>

### <span data-ttu-id="71c07-134">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="71c07-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="71c07-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="71c07-135">NOTES</span></span>

## <span data-ttu-id="71c07-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71c07-136">RELATED LINKS</span></span>

[<span data-ttu-id="71c07-137">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="71c07-137">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="71c07-138">Neu – AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="71c07-138">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="71c07-139">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="71c07-139">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)


